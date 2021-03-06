Power Test
----------

* Seed: 601232222

+------------------+----------------------+----------------------+----------------------+
|Duration (seconds)|Query Start Time      |RF1 Start Time        |RF2 Start Time        |
|                  +----------------------+----------------------+----------------------+
|                  |Query End Time        |RF1 End Time          |RF2 End Time          |
+==================+======================+======================+======================+
|            216.21|2022-06-01 23:22:43.55|2022-06-01 23:22:26.91|2022-06-01 23:26:02.94|
|                  +----------------------+----------------------+----------------------+
|                  |2022-06-01 23:26:02.72|2022-06-01 23:22:43.54|2022-06-01 23:26:03.10|
+------------------+----------------------+----------------------+----------------------+

=====  =======================
Query  Response Time (seconds)
=====  =======================
    1  31.50
    2  4.42
    3  10.99
    4  1.57
    5  10.42
    6  4.43
    7  7.76
    8  2.39
    9  18.41
   10  9.18
   11  1.67
   12  8.73
   13  27.21
   14  4.40
   15  11.09
   16  3.45
   17  0.11
   18  31.19
   19  0.14
   20  2.89
   21  5.04
   22  0.46
  RF1  16.63
  RF2  0.16
=====  =======================

Throughput Test
---------------

Stream execution summary:

+---------+---------+----------------------+----------------------+----------------------+
|Stream   |Duration |Query Start Time      |RF1 Start Time        |RF2 Start Time        |
+---------+(seconds)+----------------------+----------------------+----------------------+
|Seed     |         |Query End Time        |RF1 End Time          |RF2 End Time          |
+=========+=========+======================+======================+======================+
|        1|   499.24|2022-06-01 23:26:21.62|2022-06-01 23:26:04.48|2022-06-01 23:26:45.84|
+---------+         +----------------------+----------------------+----------------------+
|601232223|         |2022-06-01 23:26:50.20|2022-06-01 23:26:45.75|2022-06-01 23:26:46.80|
+---------+---------+----------------------+----------------------+----------------------+
|        2|   490.30|2022-06-01 23:26:04.75|2022-06-01 23:26:46.86|2022-06-01 23:27:30.45|
+---------+         +----------------------+----------------------+----------------------+
|601232224|         |2022-06-01 23:26:16.41|2022-06-01 23:27:30.37|2022-06-01 23:27:31.55|
+---------+---------+----------------------+----------------------+----------------------+
|        3|   491.61|2022-06-01 23:26:04.75|2022-06-01 23:27:31.71|2022-06-01 23:28:12.06|
+---------+         +----------------------+----------------------+----------------------+
|601232225|         |2022-06-01 23:26:11.05|2022-06-01 23:28:11.97|2022-06-01 23:28:13.29|
+---------+---------+----------------------+----------------------+----------------------+

Query execution duration (seconds):

======  =======  =======  =======  =======  =======  =======  =======
Stream  Q1       Q2       Q3       Q4       Q5       Q6       Q7     
======  =======  =======  =======  =======  =======  =======  =======
     1    62.60    11.57    28.58     1.34    30.22    13.08    25.72
     2    59.63    16.76    29.10     4.19    27.22    11.66    18.31
     3    73.72    12.25    24.12     5.36    27.28    14.05    20.05
   Min    59.63    11.57    24.12     1.34    27.22    11.66    18.31
   Max    73.72    16.76    29.10     5.36    30.22    14.05    25.72
   Avg    65.32    13.53    27.27     3.63    28.24    12.93    21.36
======  =======  =======  =======  =======  =======  =======  =======

======  =======  =======  =======  =======  =======  =======  =======
Stream  Q8       Q9       Q10      Q11      Q12      Q13      Q14    
======  =======  =======  =======  =======  =======  =======  =======
     1     6.35    48.58    21.26     7.96    22.24    65.33    12.20
     2     7.47    69.91    25.65     6.36    19.38    68.19    11.94
     3     6.30    41.32    18.81     4.37    25.43    79.16    12.23
   Min     6.30    41.32    18.81     4.37    19.38    65.33    11.94
   Max     7.47    69.91    25.65     7.96    25.43    79.16    12.23
   Avg     6.70    53.27    21.91     6.23    22.35    70.89    12.12
======  =======  =======  =======  =======  =======  =======  =======

======  =======  =======  =======  =======  =======  =======  =======
Stream  Q15      Q16      Q17      Q18      Q19      Q20      Q21    
======  =======  =======  =======  =======  =======  =======  =======
     1    27.69     6.71     0.26    77.03     0.59     7.32    16.76
     2    22.54    10.51     0.35    53.94     0.64     7.61    15.94
     3    27.53     6.35     0.42    62.81     0.36     8.44    14.80
   Min    22.54     6.35     0.26    53.94     0.36     7.32    14.80
   Max    27.69    10.51     0.42    77.03     0.64     8.44    16.76
   Avg    25.92     7.86     0.34    64.59     0.53     7.79    15.83
======  =======  =======  =======  =======  =======  =======  =======

======  =======  =======  =======
Stream  Q22      RF1      RF2
======  =======  =======  =======
     1     1.07    41.27     0.96
     2     1.28    43.50     1.09
     3     1.74    40.26     1.23
   Min     1.07    40.26     0.96
   Max     1.74    43.50     1.23
   Avg     1.36    41.68     1.09
======  =======  =======  =======
