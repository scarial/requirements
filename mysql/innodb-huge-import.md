# Import huge files

Use tools that can parallelize executions : 
- mydumper => https://github.com/maxbube/mydumper
- myloader => https://github.com/zhangjinpeng1987/myloader


## InnoDB

1. Connect to the right database in mysql

2. Execute commands 
```
mysql> set autocommit=0; set unique_checks=0; set foreign_key_checks=0;
mysql> source /path/to/dump.sql
mysql> commit; set unique_checks=1; set foreign_key_checks=1;
```
