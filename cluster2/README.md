# MYSQL主从2 - 配置

## 1、连接到master的mysql，并创建用于从机同步连接的账号

``` sql
# 创建用于slave连接的账号
create user 'slave'@'%' identified by '123456';

# 授权
grant replication slave on *.* to 'slave'@'%';

flush privileges;

# 查看master状态
show master status;

```
## 2、连接slave的mysql

```sql
CHANGE MASTER TO 
master_host='192.168.0.104',  
master_port=13306, 
master_user='slave', 
master_password='123456', 
master_log_file='mysql-bin.000003', 
master_log_pos=925;

# master_log_file和master_log_pos 可以通过在master中show master status查看到

# 启动slave

start slave;

# 查看slave状态
show slave status;

```
