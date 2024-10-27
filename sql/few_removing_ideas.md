## When you need to remove N*1000 records from DB

1. remove one by one
2. use partitions for tables and remove old partition. 1 operation removes many records at the same time
