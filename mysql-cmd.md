# MySQL command 的記錄

## mysql.exe
- select
```
C:\xampp\mysql\bin>mysql -uyourname -pyourpwd -Ddbname -e "select * from csv_test"
+---------------------+------+
| time                | data |
+---------------------+------+
| 2018-06-17 10:14:00 | 10   |
| 2018-06-17 10:14:05 | 12   |
| 2018-06-17 10:14:10 | 8    |
| 2018-06-17 10:14:15 | 10   |
+---------------------+------+
```

- select 轉出為csv, 不知為何就是會有access denied, 若有人知道再請告訴我...
```
C:\xampp\mysql\bin>mysql -uyourname -pyourpwd -Ddbname -e "select * from csv_test int
o outfile 'e:/csvtest.csv'"
ERROR 1045 (28000) at line 1: Access denied for user 'yourname'@'localhost' (using
 password: YES)
```
