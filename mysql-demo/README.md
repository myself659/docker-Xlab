
# 说明  

## build 
```
docker  build  -t  mysql-demo .
```

## run 

```
docker run  -d  -p 13306:3306 --name  mysql-demo -e MYSQL_ROOT_PASSWORD=123123123 mysql-demo
```

## show 

```
docker ps  
```

## docker bash  

```
 docker exec  -it  mysql-demo  bash
```

## stop 

```
docker  stop  mysql-demo 
docker  rm  mysql-demo  
```
## volume

```
docker run  -d  -p 13306:3306 --name  mysql-demo -v h:/DockerData/company:/var/lib/mysql  -e MYSQL_ROOT_PASSWORD=123123123 mysql-demo
```

## debug 

```
docker run  --entrypoint /bin/bash    -p 13306:3306 --name  mysql-demo -v h:/DockerData/company:/var/lib/mysql  -e MYSQL_ROOT_PASSWORD=123123123 mysql-demo -s
```


## custom 

```
docker run  -d  -p 13306:3306 --name  mysql-demo -v ./sql_scripts:/docker-entrypoint-initdb.d/ -e MYSQL_ROOT_PASSWORD=123123123 mysql-demo
```


# 控制docker版本 

```
FROM mysql:5.7
```

# backup  

[How to backup a MySQL database using Docker](https://devopsheaven.com/mysql/mysqldump/databases/docker/backup/2017/09/17/backup-mysql-database-using-docker.html)

