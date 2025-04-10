Data Format
===========

The measurement files are stored in H5 file format. For each scenario
there are two files. The channel file includes the channel frequency
response and the estimated delay and Doppler of the target, together
with the positions of the receiver antennas. The target file includes
the localization information (position, velocity, and acceleration) from
an on-board RTK receiver. The timestamps of the data are available in
both files as metadata.

In order to distinguish between different scenarios and and also
simplify accessing the UAV routes the measurement files are cropped into
smaller files that hold to the following naming convention:

``<Start Point [int]> to <End Point [int]> _H <Height [m]> _V<Target velocity [m/s]>.h5``

The values for ``Start Point`` and ``End Point`` are illustrated on the
interactive trajectory map below. Click the markers to see a label and
description.

.. raw:: html

   <p>

See full screen

.. raw:: html

   </p>

{: .info} The velocity stated in the scenario name is not the actual
velocity of the UAV, but rather the maximum velocity of the target UAV.
Use the groundtruth files to check the RTK measured velocity at all
available snapshots.

Data Structure
--------------

The structure of the ``*.h5`` files is illustrated in the following
figures. For programmatic examples how to read the files, please refer
to `Examples </3-examples.markdown>`__.

Channel File Structure
----------------------

.. figure:: /static/isacuavdataset/treeview-2.png
   :alt: H5 Channel File Structure

   H5 Channel File Structure

Target File Structure
---------------------

.. figure:: /static/isacuavdataset/treeview-3.png
   :alt: H5 Target File Structure

   H5 Target File Structure

Available Scenarios
-------------------

{: .note} In general, each scenario was flown at a height of 15 m and 30
m **and** at a maximum velocity of 5 m/s and 11 m/s.

Here is a full list of all available scenarios. The names in the list
can also be used to query the scenarios in the ``downloader.py``.

============== =============== ============== ===============
h=15 m, v=5m/s h=15 m, v=11m/s h=30 m, v=5m/s h=30 m, v=11m/s
============== =============== ============== ===============
0to1_H15_V5    1to2_H15_V11    1to2_H30_V5    1to0_H30_V11
0to9_H15_V5    2to1_H15_V11    2to1_H30_V5    1to2_H30_V11
1to2_H15_V5    2to3_H15_V11    2to3_H30_V5    2to1_H30_V11
2to1_H15_V5    3to2_H15_V11    3to2_H30_V5    2to3_H30_V11
2to3_H15_V5    3to4_H15_V11    3to4_H30_V5    3to2_H30_V11
3to2_H15_V5    4to3_H15_V11    4to3_H30_V5    3to4_H30_V11
3to4_H15_V5    4to5_H15_V11    4to5_H30_V5    4to3_H30_V11
4to3_H15_V5    5to4_H15_V11    5to4_H30_V5    4to5_H30_V11
4to5_H15_V5    5to6_H15_V11    5to6_H30_V5    5to4_H30_V11
5to4_H15_V5    6to5_H15_V11    6to5_H30_V5    5to6_H30_V11
5to6_H15_V5    6to7_H15_V11    6to7_H30_V5    6to5_H30_V11
6to5_H15_V5    7to6_H15_V11    7to6_H30_V5    6to7_H30_V11
6to7_H15_V5    7to8_H15_V11    7to8_H30_V5    7to6_H30_V11
7to6_H15_V5    8to7_H15_V11    8to7_H30_V5    7to8_H30_V11
7to8_H15_V5                                   8to7_H30_V11
8to7_H15_V5                                   
============== =============== ============== ===============
