Measurement Campaign
====================

This site introduces the measurement campaign that was conducted to
obtain the measurement data for the ISAC dataset. We focus on the
details relevant to the dataset and refer to [1] for a more detailed
description of the measurement setup.

Measurement Impressions
-----------------------

Flight area for the measurement in Ilmenau, Germany. |Flight Area|

Hardware and Signal Parameters
------------------------------

The following signal parameters were used in the Software-Defined-Radios
(SDRs). During the measurement, a single transmitter would send a
contniuous, OFDM-like signal, that is captured by the three receivers
VGH0, VGH1, and VGH2. All antennas were placed on the roof of an urban
building, with the UAV flying in the vicinity of the building.

.. figure:: /static/isacuavdataset/fhg-antenna.png
   :alt: Antenna Placement on FhG building

   Antenna Placement on FhG building

{: .note} The data **RadioLab** Rx is currently not part of the dataset.

======================== ===============
Parameter                Value
======================== ===============
Center Frequency         3.75 GHz
Sampling Rate Tx         100 MSPS
Sampling Rate Rx         100 MSPS
Bandwidth                80 MHz
Symbol Length            16
                         
                         .. math:: \mu s
Subcarriers (used/total) 1280/1600
======================== ===============

Below are the antenna positions for the measurement campaign. The
position of each Rx antenna was measured with the RTK receiver over a
period of at leat 1 minute, recording ~ 600 positions. To obtain the
positions below, the first and last 100 values were discarded and the
remaining values were averaged.

+------------------+----------------+-----------------+----------------+
|                  | VGH0           | VGH1            | VGH2           |
+==================+================+=================+================+
| Latitude [deg]   | 50.6           | 50              | 50.            |
|                  | 93345516466685 | .69341057007242 | 69360674942051 |
+------------------+----------------+-----------------+----------------+
| Longitude [deg]  | 10.9           | 10.             | 10.9           |
|                  | 36996650225382 | 936834788086342 | 36350730986371 |
+------------------+----------------+-----------------+----------------+
| Height [mm]      | 565            | 56              | 565            |
|                  | 181.7282539684 | 5180.4359331481 | 349.6034090916 |
+------------------+----------------+-----------------+----------------+
| rel. Pos. East   | -119           | -130            | -164           |
| [cm]             | 17.87336507936 | 61.664401114216 | 82.21163636364 |
+------------------+----------------+-----------------+----------------+
| rel. Pos. North  | 1238           | 124             | 1267           |
| [cm]             | 42.51892063505 | 566.28231197789 | 48.91054545464 |
+------------------+----------------+-----------------+----------------+
| rel. Pos. Down   | -527           | -52             | -529           |
| [cm]             | 6.027650793646 | 75.735403899723 | 2.143045454549 |
+------------------+----------------+-----------------+----------------+

Groundtruth
-----------

To evaluate the localization results, the groundtruth position of the
UAV is recorded with a u-blox ZED-F9P RTK dual-band GNSS receiver. Since
all of the positions of the antennas and the target is measured using
RTK methods the locations are reported in N/E/D or E/N/U coordinate
system with the position of the SAPOS base station as the reference. The
used SAPOS base station is located at (WGS-84)

::

   - 50.681024198 deg N, 
   - 10.934963069 deg E, 
   - 550.2006 m

| {: .fs-3}
| **References**

{: .fs-2} [1] - Measurement Testbed for Radar and Emitter Localization
of UAV at 3.75 GHz, Julia Beuster, Carsten Andrich, Michael Döbereiner,
Steffen Schieler, Maximilian Engelhardt, Christian Schneider, and Reiner
Thomä, 17th European Conference on Antennas and Propagation (EuCAP),
2023, DOI: 10.23919/EuCAP57121.2023.10133118

.. |Flight Area| image:: /static/isacuavdataset/impressions/flight_area.jpg
