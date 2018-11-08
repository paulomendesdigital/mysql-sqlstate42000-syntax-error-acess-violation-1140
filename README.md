# Error: SQLSTATE[42000]: Syntax error or acess violation: 1140

Access the file mysqld.cnf
```
sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf
```

Add the line above at the end
```
sql_mode = "STRICT_TRANS_TABLES,ERROR_FOR_DIVISION_BY_ZERO,NO_AUTO_CREATE_USER,NO_ENGINE_SUBSTITUTION"
```

Restart mysql
```
sudo /etc/init.d/mysql restart
```
