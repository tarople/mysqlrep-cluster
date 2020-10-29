# 基于haproxy、mycat、mysql主从集群

### 包含容器

* cluster1和cluster2中分别包含3个mysql容器，一个master和两个slave
* mycat1和mycat2
* haproxy

### 下载

~~~bash

git clone https://github.com/tarople/mysqlrep-cluster.git

~~~

### 说明

#### 1、mysql

  > 如需要做多个mysql主从，可复制cluster1,并修改docker-compose.yml的相关配置

#### 2、mycat

  > 如需要做多个mycat，可复制mycat1,并修改docker-compose.yml的相关配置

### 启动容器

> 1、进入子目录
> 2、启动顺序为[cluster1](https://github.com/tarople/mysqlrep-cluster/tree/master/cluster1)、[cluster2](https://github.com/tarople/mysqlrep-cluster/tree/master/cluster2) -> [mycat1](https://github.com/tarople/mysqlrep-cluster/tree/master/mycat1)、[mycat2](https://github.com/tarople/mysqlrep-cluster/tree/master/mycat2) -> [haproxy](https://github.com/tarople/mysqlrep-cluster/tree/master/haproxy)
