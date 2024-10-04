---
layout: default
title: BigQuery Table Expiration
permalink: /bigquery/table_expiration.html
parent: BigQuery
---

BigQuery bills can pile up rapidly if you have a large userbase. To avoid this, you can utilize the table partitioning and expiration options.

Partitioning creates a new partition for every day/hour/minute so you can only query the partitions you want. If you refresh your data models everyday, you can simple query the date partition for the day before.

Things brings down processing to a fraction of the original table. 

You can also minimise the data storage with letting older data expire.

> <div markdown="block">
> {: .warning }
> Once the data expired, it will no longer be available for querying.
> </div>


But we often don't look at data older than 6 months or an year, so it's okay to let it expire in most cases.

To do this, you have to -
- Create a paritioned table
- set a partition expiry date with the code

```
ALTER TABLE mydataset.mytable
  SET OPTIONS (
    -- Sets partition expiration to 5 days
    partition_expiration_days = 5);
```
Fore more details, [visit bigquery](https://cloud.google.com/bigquery/docs/managing-partitioned-tables#update_the_partition_expiration)
