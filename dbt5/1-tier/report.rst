======================
Database Test 5 Report
======================

**These results are not comparable to TPC Benchmark(TM) E results.**

Summary
=======

* Date: Tue Feb  6 11:26:04 CST 2024
* Scale Factor: 500

==========================================  ==================================
Reported Throughput:            3.16 trtps  Configured Customers:         5000
==========================================  ==================================

==================  ==========  ==========  ==========  ==========
Response Times (s)     Minimum     Average  90th %tile     Maximum
==================  ==========  ==========  ==========  ==========
     Broker Volume        0.00        0.00        0.00        0.03
 Customer Position        0.00        3.50       10.26       32.60
       Market Feed        0.03        0.18        0.33        0.53
      Market Watch        0.00        0.12        0.24        0.51
   Security Detail        0.00        0.07        0.15        0.32
      Trade Lookup        0.14       18.31       56.13       63.31
       Trade Order        0.00        0.06        0.15        0.31
      Trade Result        0.00        0.07        0.19        0.52
      Trade Status        0.01        7.35       15.93       42.44
      Trade Update        0.21       15.15       49.24       57.57
  Data Maintenance        0.00        0.09         N/A        0.89
==================  ==========  ==========  ==========  ==========

==================  ==========  ==========  ==========  ==========  ==========
   Transaction Mix   Txn Count   Mix %tile  Rollbacks     Warnings     Invalid
==================  ==========  ==========  ==========  ==========  ==========
     Broker Volume         101       4.978           0           0           0
 Customer Position         254      12.518           0           0           0
       Market Feed          19       0.936           0           0           0
      Market Watch         352      17.348           0           0           0
   Security Detail         276      13.603           0           0           0
      Trade Lookup         159       7.836           0           0           0
       Trade Order         204      10.054           2           0           0
      Trade Result         190       9.364           0           0           0
      Trade Status         370      18.236           0           0           0
      Trade Update          38       1.873           0           0           0
  Data Maintenance          60         N/A           0           0           0
==================  ==========  ==========  ==========  ==========  ==========

==================================================================  ==========
Test Duration and Timings
==================================================================  ==========
                                            Ramp-up Time (minutes)         0.0
                                    Measurement Interval (minutes)        60.1
    Total Number of Transactions Completed in Measurement Interval        2029
==================================================================  ==========

Notes: 

Transaction Charts
==================

+-----------+----------------------------------------+------------------------------------+
|Transaction|            Response Time               |        Time Distribution           |
+===========+========================================+====================================+
|Security   |.. image:: txn/t0-transaction-rate.png  |.. image:: txn/t0-distribution.png  |
|Detail     |   :target: txn/t0-transaction-rate.png |   :target: txn/t0-distribution.png |
|           |   :width: 100%                         |   :width: 100%                     |
+-----------+----------------------------------------+------------------------------------+
|Broker     |.. image:: txn/t1-transaction-rate.png  |.. image:: txn/t1-distribution.png  |
|Volume     |   :target: txn/t1-transaction-rate.png |   :target: txn/t1-distribution.png |
|           |   :width: 100%                         |   :width: 100%                     |
+-----------+----------------------------------------+------------------------------------+
|Customer   |.. image:: txn/t2-transaction-rate.png  |.. image:: txn/t2-distribution.png  |
|Position   |   :target: txn/t2-transaction-rate.png |   :target: txn/t2-distribution.png |
|           |   :width: 100%                         |   :width: 100%                     |
+-----------+----------------------------------------+------------------------------------+
|Market     |.. image:: txn/t3-transaction-rate.png  |.. image:: txn/t3-distribution.png  |
|Watch      |   :target: txn/t3-transaction-rate.png |   :target: txn/t3-distribution.png |
|           |   :width: 100%                         |   :width: 100%                     |
+-----------+----------------------------------------+------------------------------------+
|Trade      |.. image:: txn/t4-transaction-rate.png  |.. image:: txn/t4-distribution.png  |
|Status     |   :target: txn/t4-transaction-rate.png |   :target: txn/t4-distribution.png |
|           |   :width: 100%                         |   :width: 100%                     |
+-----------+----------------------------------------+------------------------------------+
|Trade      |.. image:: txn/t5-transaction-rate.png  |.. image:: txn/t5-distribution.png  |
|Lookup     |   :target: txn/t5-transaction-rate.png |   :target: txn/t5-distribution.png |
|           |   :width: 100%                         |   :width: 100%                     |
+-----------+----------------------------------------+------------------------------------+
|Trade      |.. image:: txn/t6-transaction-rate.png  |.. image:: txn/t6-distribution.png  |
|Order      |   :target: txn/t6-transaction-rate.png |   :target: txn/t6-distribution.png |
|           |   :width: 100%                         |   :width: 100%                     |
+-----------+----------------------------------------+------------------------------------+
|Trade      |.. image:: txn/t7-transaction-rate.png  |.. image:: txn/t7-distribution.png  |
|Update     |   :target: txn/t7-transaction-rate.png |   :target: txn/t7-distribution.png |
|           |   :width: 100%                         |   :width: 100%                     |
+-----------+----------------------------------------+------------------------------------+
|Market     |.. image:: txn/t8-transaction-rate.png  |.. image:: txn/t8-distribution.png  |
|Feed       |   :target: txn/t8-transaction-rate.png |   :target: txn/t8-distribution.png |
|           |   :width: 100%                         |   :width: 100%                     |
+-----------+----------------------------------------+------------------------------------+
|Trade      |.. image:: txn/t9-transaction-rate.png  |.. image:: txn/t9-distribution.png  |
|Result     |   :target: txn/t9-transaction-rate.png |   :target: txn/t9-distribution.png |
|           |   :width: 100%                         |   :width: 100%                     |
+-----------+----------------------------------------+------------------------------------+
|Data       |.. image:: txn/t10-transaction-rate.png |.. image:: txn/t10-distribution.png |
|Maintenance|   :target: txn/t10-transaction-rate.png|   :target: txn/t10-distribution.png|
|           |   :width: 100%                         |   :width: 100%                     |
+-----------+----------------------------------------+------------------------------------+

System Summary
==============

.. list-table::
   :header-rows: 1

   * -
     - Operating System
     - Charts
     - Profiling
   * - **Database System**
     -
     -
     -
   * - z15rhel7
     - Linux z15rhel7 3.10.0-1160.71.1.el7.s390x #1 SMP Wed Jun 15 04:53:41 EDT 2022 s390x s390x s390x GNU/Linux
     - `CPU <db/z15rhel7/cpu/>`__ `Memory <db/z15rhel7/mem/>`__ `Blockdev <db/z15rhel7/blockdev/>`__ `Network <db/z15rhel7/net/>`__ `Paging <db/z15rhel7/paging/>`__ `Swap <db/z15rhel7/swap/>`__
     - 

Component Statistics per Process
--------------------------------

Driver(s):

Customer Emulator(s):

Market Exchange Emulator(s):

Database System(s):

* z15rhel7
   * `DriverMain <db/z15rhel7/DriverMain/>`__
   * `BrokerageHouseMain <db/z15rhel7/BrokerageHouseMain/>`__
   * `MarketExchangeMain <db/z15rhel7/MarketExchangeMain/>`__
