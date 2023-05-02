======================
Database Test 2 Report
======================

**These results are not comparable to TPC Benchmark(TM) C Results.**

Summary
=======

* Date: Fri Apr 28 04:39:41 PM PDT 2023
* Scale Factor: 10 warehouses
* DBMS: PostgreSQL 14.3 on x86_64-redhat-linux-gnu, compiled by gcc (GCC) 12.1.1 20220628 (Red Hat 12.1.1-3), 64-bit

============  =====  =========  =========  ===========  ===========  =====
          ..     ..    Response Time (s)            ..           ..     ..
------------  -----  --------------------  -----------  -----------  -----
 Transaction      %   Average     90th %        Total    Rollbacks      %
============  =====  =========  =========  ===========  ===========  =====
    Delivery   4.01      0.011      0.016        18712            0   0.00
   New Order  44.91      0.009      0.013       209637         2092   1.00
Order Status   3.97      0.004      0.007        18522            0   0.00
     Payment  43.08      0.006      0.009       201097            0   0.00
 Stock Level   4.04      0.004      0.005        18852            0   0.00
============  =====  =========  =========  ===========  ===========  =====

* Throughput: 3493.95 new-order transactions per minute (NOTPM)
* Duration: 60.0 minute(s)
* Unknown Errors: 0
* Ramp Up Time: 0.0 minute(s)

Notes: 

Transaction Charts
==================

+------------+---------------------------------------+-----------------------------------+
|Transaction |            Response Time              |        Time Distribution          |
+============+=======================================+===================================+
|Delivery    |.. image:: txn/td-transaction-rate.png |.. image:: txn/td-distribution.png |
|            |   :target: txn/td-transaction-rate.png|   :target: txn/td-distribution.png|
|            |   :width: 100%                        |   :width: 100%                    |
+------------+---------------------------------------+-----------------------------------+
|New Order   |.. image:: txn/tn-transaction-rate.png |.. image:: txn/tn-distribution.png |
|            |   :target: txn/tn-transaction-rate.png|   :target: txn/tn-distribution.png|
|            |   :width: 100%                        |   :width: 100%                    |
+------------+---------------------------------------+-----------------------------------+
|Order Status|.. image:: txn/to-transaction-rate.png |.. image:: txn/to-distribution.png |
|            |   :target: txn/to-transaction-rate.png|   :target: txn/to-distribution.png|
|            |   :width: 100%                        |   :width: 100%                    |
+------------+---------------------------------------+-----------------------------------+
|Payment     |.. image:: txn/tp-transaction-rate.png |.. image:: txn/tp-distribution.png |
|            |   :target: txn/tp-transaction-rate.png|   :target: txn/tp-distribution.png|
|            |   :width: 100%                        |   :width: 100%                    |
+------------+---------------------------------------+-----------------------------------+
|Stock Level |.. image:: txn/ts-transaction-rate.png |.. image:: txn/ts-distribution.png |
|            |   :target: txn/ts-transaction-rate.png|   :target: txn/ts-distribution.png|
|            |   :width: 100%                        |   :width: 100%                    |
+------------+---------------------------------------+-----------------------------------+

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
     - GNU/Linux x86_64 6.1.12-200.fc37.x86_64
     - `CPU <driver/potassium/cpu/>`__ `Memory <driver/potassium/mem/>`__ `Blockdev <driver/potassium/blockdev/>`__ `Network <driver/potassium/net/>`__ `Paging <driver/potassium/paging/>`__ `Swap <driver/potassium/swap/>`__
     - `perf-report <driver/potassium/profile/perf-report.txt>`__ `perf-trace <driver/potassium/profile/perf-trace.txt>`__ `perf-annotated-source <driver/potassium/profile/perf-annotate.txt>`__ `flame-graph <driver/potassium/profile/flamegraph.svg>`__ 
   * - **Client System(s)**
     -
     -
     -
   * - **Database System(s)**
     -
     -
     -
   * - lithium
     - GNU/Linux x86_64 6.1.12-200.fc37.x86_64
     - `CPU <db/lithium/cpu/>`__ `Memory <db/lithium/mem/>`__ `Blockdev <db/lithium/blockdev/>`__ `Network <db/lithium/net/>`__ `Paging <db/lithium/paging/>`__ `Swap <db/lithium/swap/>`__
     - `perf-report <db/lithium/profile/perf-report.txt>`__ `perf-trace <db/lithium/profile/perf-trace.txt>`__ `perf-annotated-source <db/lithium/profile/perf-annotate.txt>`__ `flame-graph <db/lithium/profile/flamegraph.svg>`__ 

Component Statistics per Process
--------------------------------

Driver System(s):

* potassium
   * `driver <driver/potassium/driver/>`__

Client System(s):

Database System(s):

* lithium

PostgreSQL Report
=================

lithium
--------------------------------------------------------------------------------

* `Database Parameters <db/lithium/dbstat/params.csv>`__
* `Query plans <db/lithium/plan0.txt>`__

.. list-table::

   * - Database Stats Charts
     - `dbt2 <db/lithium/dbstat/db/dbt2>`__
   * - Database Table Stats Charts:
     - `public.customer <db/lithium/dbstat/table/public.customer/>`__ `public.district <db/lithium/dbstat/table/public.district/>`__ `public.history <db/lithium/dbstat/table/public.history/>`__ `public.item <db/lithium/dbstat/table/public.item/>`__ `public.new_order <db/lithium/dbstat/table/public.new_order/>`__ `public.order_line <db/lithium/dbstat/table/public.order_line/>`__ `public.orders <db/lithium/dbstat/table/public.orders/>`__ `public.stock <db/lithium/dbstat/table/public.stock/>`__ `public.warehouse <db/lithium/dbstat/table/public.warehouse/>`__ 
   * - Database Index Stats Charts:
     - `public.customer.i_customer <db/lithium/dbstat/index/public.customer.i_customer/>`__ `public.orders.i_orders <db/lithium/dbstat/index/public.orders.i_orders/>`__ `public.customer.pk_customer <db/lithium/dbstat/index/public.customer.pk_customer/>`__ `public.district.pk_district <db/lithium/dbstat/index/public.district.pk_district/>`__ `public.item.pk_item <db/lithium/dbstat/index/public.item.pk_item/>`__ `public.new_order.pk_new_order <db/lithium/dbstat/index/public.new_order.pk_new_order/>`__ `public.order_line.pk_order_line <db/lithium/dbstat/index/public.order_line.pk_order_line/>`__ `public.orders.pk_orders <db/lithium/dbstat/index/public.orders.pk_orders/>`__ `public.stock.pk_stock <db/lithium/dbstat/index/public.stock.pk_stock/>`__ `public.warehouse.pk_warehouse <db/lithium/dbstat/index/public.warehouse.pk_warehouse/>`__ 
   * - Database Tables by Metric:
     - `analyze_count <db/lithium/dbstat/table-stat/t_analyze_count/>`__ `autoanalyze_count <db/lithium/dbstat/table-stat/t_autoanalyze_count/>`__ `autovacuum_count <db/lithium/dbstat/table-stat/t_autovacuum_count/>`__ `heap_blks_hit <db/lithium/dbstat/table-stat/t_heap_blks_hit/>`__ `heap_blks_read <db/lithium/dbstat/table-stat/t_heap_blks_read/>`__ `idx_blks_hit <db/lithium/dbstat/table-stat/t_idx_blks_hit/>`__ `idx_blks_read <db/lithium/dbstat/table-stat/t_idx_blks_read/>`__ `idx_scan <db/lithium/dbstat/table-stat/t_idx_scan/>`__ `idx_tup_fetch <db/lithium/dbstat/table-stat/t_idx_tup_fetch/>`__ `n_dead_tup <db/lithium/dbstat/table-stat/t_n_dead_tup/>`__ `n_ins_since_vacuum <db/lithium/dbstat/table-stat/t_n_ins_since_vacuum/>`__ `n_live_tup <db/lithium/dbstat/table-stat/t_n_live_tup/>`__ `n_mod_since_analyze <db/lithium/dbstat/table-stat/t_n_mod_since_analyze/>`__ `n_tup_del <db/lithium/dbstat/table-stat/t_n_tup_del/>`__ `n_tup_hot_upd <db/lithium/dbstat/table-stat/t_n_tup_hot_upd/>`__ `n_tup_ins <db/lithium/dbstat/table-stat/t_n_tup_ins/>`__ `n_tup_upd <db/lithium/dbstat/table-stat/t_n_tup_upd/>`__ `seq_scan <db/lithium/dbstat/table-stat/t_seq_scan/>`__ `seq_tup_read <db/lithium/dbstat/table-stat/t_seq_tup_read/>`__ `tidx_blks_hit <db/lithium/dbstat/table-stat/t_tidx_blks_hit/>`__ `tidx_blks_read <db/lithium/dbstat/table-stat/t_tidx_blks_read/>`__ `toast_blks_hit <db/lithium/dbstat/table-stat/t_toast_blks_hit/>`__ `toast_blks_read <db/lithium/dbstat/table-stat/t_toast_blks_read/>`__ `vacuum_count <db/lithium/dbstat/table-stat/t_vacuum_count/>`__ 
   * - Database Indexs by Metric:
     - `idx_blks_hit <db/lithium/dbstat/index-stat/i_idx_blks_hit/>`__ `idx_blks_read <db/lithium/dbstat/index-stat/i_idx_blks_read/>`__ `idx_scan <db/lithium/dbstat/index-stat/i_idx_scan/>`__ `idx_tup_fetch <db/lithium/dbstat/index-stat/i_idx_tup_fetch/>`__ `idx_tup_read <db/lithium/dbstat/index-stat/i_idx_tup_read/>`__ 

Per Process Statistics
----------------------

* `autovacuum <db/lithium/sysstat/autovacuum/>`__
* `bgwriter <db/lithium/sysstat/bgwriter/>`__
* `checkpointer <db/lithium/sysstat/checkpointer/>`__
* `logger <db/lithium/sysstat/logger/>`__
* `logical <db/lithium/sysstat/logical/>`__
* `statscollector <db/lithium/sysstat/statscollector/>`__
* `walwriter <db/lithium/sysstat/walwriter/>`__
