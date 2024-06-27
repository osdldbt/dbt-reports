=========================
Database Test 7 Load Test
=========================

================  ===================  ===================  ===============
Phase             Start Timestamp      End Timestamp        Elapsed Time
================  ===================  ===================  ===============
           TABLE  2024-06-27 03:05:05  2024-06-27 03:05:31  00:00:25.566533
           INDEX  2024-06-27 03:05:31  2024-06-27 03:05:36  00:00:04.61405
         ANALYZE  2024-06-27 03:05:36  2024-06-27 03:05:39  00:00:03.655999
        LOADTEST  2024-06-27 03:05:05  2024-06-27 03:05:39  00:00:33.988806
================  ===================  ===================  ===============

System Statistics
=================

Processor Statistics
--------------------

.. image:: load/sar/sar-cpu-all-busy.png
   :width: 100%

Block Device Statistics
-----------------------

.. image:: load/sar/sar-blockdev-all-aqu-sz.png
   :width: 100%

.. image:: load/sar/sar-blockdev-all-areq-sz.png
   :width: 100%

.. image:: load/sar/sar-blockdev-all-wkB_s.png
   :width: 100%

.. image:: load/sar/sar-blockdev-all-tps.png
   :width: 100%

.. image:: load/sar/sar-blockdev-all-rkB_s.png
   :width: 100%

.. image:: load/sar/sar-blockdev-all-await.png
   :width: 100%

.. image:: load/sar/sar-blockdev-all-dkB_s.png
   :width: 100%

.. image:: load/sar/sar-blockdev-all-util.png
   :width: 100%
