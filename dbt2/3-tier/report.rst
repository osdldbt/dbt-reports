======================
Database Test 2 Report
======================

**These results are not comparable to TPC Benchmark(TM) C Results.**

Summary
=======

Mon Apr 25 13:15:59 UTC 2022

============  =====  =========  =========  ===========  ===========  =====
          ..     ..    Response Time (s)            ..           ..     ..
------------  -----  --------------------  -----------  -----------  -----
 Transaction      %   Average     90th %        Total    Rollbacks      %
============  =====  =========  =========  ===========  ===========  =====
    Delivery   4.00      0.007      0.011        19167            0   0.00
   New Order  44.99      0.003      0.004       215560         2098   0.97
Order Status   4.00      0.001      0.002        19162            0   0.00
     Payment  42.96      0.010      0.020       205875            0   0.00
 Stock Level   4.05      0.001      0.001        19411            0   0.00
============  =====  =========  =========  ===========  ===========  =====

* 43256.19 new-order transactions per minute (NOTPM)
* 5.0 minute duration
* 0 total unknown errors
* 0.0 minutes(s) ramping up

Notes: 

Transaction Charts
==================

+------------+--------------------------------------+-----------------------------------+
|Transaction |            Response Time             |        Time Distribution          |
+============+======================================+===================================+
|Delivery    |.. image:: txn/d-transaction-rate.png |.. image:: txn/td-distribution.png |
|            |   :target: txn/d-transaction-rate.png|   :target: txn/td-distribution.png|
|            |   :width: 100%                       |   :width: 100%                    |
+------------+--------------------------------------+-----------------------------------+
|New Order   |.. image:: txn/n-transaction-rate.png |.. image:: txn/tn-distribution.png |
|            |   :target: txn/n-transaction-rate.png|   :target: txn/tn-distribution.png|
|            |   :width: 100%                       |   :width: 100%                    |
+------------+--------------------------------------+-----------------------------------+
|Order Status|.. image:: txn/o-transaction-rate.png |.. image:: txn/to-distribution.png |
|            |   :target: txn/o-transaction-rate.png|   :target: txn/to-distribution.png|
|            |   :width: 100%                       |   :width: 100%                    |
+------------+--------------------------------------+-----------------------------------+
|Payment     |.. image:: txn/p-transaction-rate.png |.. image:: txn/tp-distribution.png |
|            |   :target: txn/p-transaction-rate.png|   :target: txn/tp-distribution.png|
|            |   :width: 100%                       |   :width: 100%                    |
+------------+--------------------------------------+-----------------------------------+
|Stock Level |.. image:: txn/s-transaction-rate.png |.. image:: txn/ts-distribution.png |
|            |   :target: txn/s-transaction-rate.png|   :target: txn/ts-distribution.png|
|            |   :width: 100%                       |   :width: 100%                    |
+------------+--------------------------------------+-----------------------------------+

System Summary
==============

.. list-table::
   :header-rows: 1

   * -
     - Operating System
     - Charts
     - Profiling
   * - **Driver System(s)**
     -
     -
     -
   * - potassium
     - GNU/Linux x86_64 5.15.32-gentoo-r1-x86_64-zbkstdxg5
     - `CPU <driver/potassium/cpu/>`__ `Memory <driver/potassium/mem/>`__ `Blockdev <driver/potassium/blockdev/>`__ `Network <driver/potassium/net/>`__ `Swap <driver/potassium/swap/>`__ 
     - `perf-report <driver/potassium/perf-report.txt>`__ `perf-trace <driver/potassium/perf-trace.txt>`__ `perf-annotated-source <driver/potassium/perf-annotate.txt>`__ `flame-graph <driver/potassium/flamegraph.svg>`__ 
   * - **Client System(s)**
     -
     -
     -
   * - sodium
     - GNU/Linux x86_64 5.15.32-gentoo-r1-x86_64-zbkstdxg5
     - `CPU <client/sodium/cpu/>`__ `Memory <client/sodium/mem/>`__ `Blockdev <client/sodium/blockdev/>`__ `Network <client/sodium/net/>`__ `Swap <client/sodium/swap/>`__ 
     - `perf-report <client/sodium/perf-report.txt>`__ `perf-trace <client/sodium/perf-trace.txt>`__ `perf-annotated-source <client/sodium/perf-annotate.txt>`__ `flame-graph <client/sodium/flamegraph.svg>`__ 
   * - **Database System(s)**
     -
     -
     -
   * - lithium
     - GNU/Linux x86_64 5.15.32-gentoo-r1-x86_64-zbkstdxg5
     - `CPU <db/lithium/cpu/>`__ `Memory <db/lithium/mem/>`__ `Blockdev <db/lithium/blockdev/>`__ `Network <db/lithium/net/>`__ `Swap <db/lithium/swap/>`__ 
     - `perf-report <db/lithium/perf-report.txt>`__ `perf-trace <db/lithium/perf-trace.txt>`__ `perf-annotated-source <db/lithium/perf-annotate.txt>`__ `flame-graph <db/lithium/flamegraph.svg>`__ 

Component Statistics per Process
--------------------------------

Driver System(s):

* potassium
   * `driver <driver/potassium/driver/>`_

Client System(s):

* sodium
   * `client <client/sodium/client/>`_

Database System(s):

* lithium

PostgreSQL Report
=================

lithium
--------------------------------------------------------------------------------

* `Database Parameters <db/lithium/param.txt>`__
* `Query plans <db/lithium/plan0.txt>`__

.. list-table::

   * - `Database Stats Charts <db/lithium/stats/>`__
     -
   * - Database Table Stats Charts:
     - `customer <db/lithium/tables/customer/>`__ `district <db/lithium/tables/district/>`__ `history <db/lithium/tables/history/>`__ `item <db/lithium/tables/item/>`__ `new_order <db/lithium/tables/new_order/>`__ `order_line <db/lithium/tables/order_line/>`__ `orders <db/lithium/tables/orders/>`__ `stock <db/lithium/tables/stock/>`__ `warehouse <db/lithium/tables/warehouse/>`__ 
   * - Database Index Stats Charts:
     - `i_customer <db/lithium/indexes/i_customer/>`__ `i_orders <db/lithium/indexes/i_orders/>`__ `pk_customer <db/lithium/indexes/pk_customer/>`__ `pk_district <db/lithium/indexes/pk_district/>`__ `pk_item <db/lithium/indexes/pk_item/>`__ `pk_new_order <db/lithium/indexes/pk_new_order/>`__ `pk_order_line <db/lithium/indexes/pk_order_line/>`__ `pk_orders <db/lithium/indexes/pk_orders/>`__ `pk_stock <db/lithium/indexes/pk_stock/>`__ `pk_warehouse <db/lithium/indexes/pk_warehouse/>`__ 
   * - Database Tables by Metric:
     - `heap_blks_hit <db/lithium/tables/t_heap_blks_hit/>`__ `heap_blks_read <db/lithium/tables/t_heap_blks_read/>`__ `idx_blks_hit <db/lithium/tables/t_idx_blks_hit/>`__ `idx_blks_read <db/lithium/tables/t_idx_blks_read/>`__ `idx_scan <db/lithium/tables/t_idx_scan/>`__ `idx_tup_fetch <db/lithium/tables/t_idx_tup_fetch/>`__ `n_dead_tup <db/lithium/tables/t_n_dead_tup/>`__ `n_live_tup <db/lithium/tables/t_n_live_tup/>`__ `n_tup_del <db/lithium/tables/t_n_tup_del/>`__ `n_tup_hot_upd <db/lithium/tables/t_n_tup_hot_upd/>`__ `n_tup_ins <db/lithium/tables/t_n_tup_ins/>`__ `n_tup_upd <db/lithium/tables/t_n_tup_upd/>`__ `seq_scan <db/lithium/tables/t_seq_scan/>`__ `seq_tup_read <db/lithium/tables/t_seq_tup_read/>`__ `tidx_blks_read <db/lithium/tables/t_tidx_blks_read/>`__ `toast_blks_hit <db/lithium/tables/t_toast_blks_hit/>`__ `toast_blks_read <db/lithium/tables/t_toast_blks_read/>`__ 
   * - Database Indexs by Metric:
     - `idx_blks <db/lithium/indexes/i_idx_blks/>`__ `idx_blks_hit <db/lithium/indexes/i_idx_blks_hit/>`__ `idx_blks_read <db/lithium/indexes/i_idx_blks_read/>`__ `idx_scan <db/lithium/indexes/i_idx_scan/>`__ `idx_tup_fetch <db/lithium/indexes/i_idx_tup_fetch/>`__ `idx_tup_read <db/lithium/indexes/i_idx_tup_read/>`__ 

Per Process Statistics
----------------------

* `autovacum <db/lithium/autovacum/>`__
* `bgwriter <db/lithium/bgwriter/>`__
* `checkpointer <db/lithium/checkpointer/>`__
* `logger <db/lithium/logger/>`__
* `logical <db/lithium/logical/>`__
* `statscollector <db/lithium/statscollector/>`__
* `walwriter <db/lithium/walwriter/>`__
