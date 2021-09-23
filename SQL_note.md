# SQL



## Table

### primary key

每個Table代表不同資料的KEY 不能重複 可以唯一表示每一筆資料

無法用一個KEY唯一代表資料 則可以設定兩個KEY一起

### foreign key

參照Table 的primary key 可以是自己也可以是別的





```mysql
CREATE DATABASE 'database_name';
SHOW DATABASES;
Drop DATABASES;
USE 'database_name';
```



```mysql
INT			--
DECIMAL(m,n)
VARCHAR(n) 	--字串
BLOB		--圖片
DATE		--YYYY-MM-DD
TIMESTAMP	--YYYY-MM-DD HH:MM:SS
```



```  mysql
CREATE TABLE 'table_name'(
	'key1' INT PRIMARY KEY,
    'key2' VARCHAR(n),
    PRIMARY KEY(key);
)
DESCRIBE 'table_name';

DROP TABLE 'table_name';

ALTER TABLE 'table_name' ADD 'key' DECIMAL(m,n);
ALTER TABLE 'table_name' DROP COLUMN 'key'

```







