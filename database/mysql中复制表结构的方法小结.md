mysql中用命令行复制表结构的方法主要有一下几种: 

1.只复制表结构到新表

    CREATE TABLE 新表 SELECT * FROM 旧表 WHERE 1=2  
或者

    CREATE TABLE 新表 LIKE 旧表  
    
2.复制表结构及数据到新表

    CREATE TABLE 新表 SELECT * FROM 旧表 

3.复制旧表的数据到新表(假设两个表结构一样) 

    INSERT INTO 新表 SELECT * FROM 旧表  

4.复制旧表的数据到新表(假设两个表结构不一样)

    INSERT INTO 新表(字段1,字段2,.......) SELECT 字段1,字段2,...... FROM 旧表 