#### 下载容器

```shell
docker pull mysql:5.7
```

#### 启动

```shell
docker run --name mysql57 -v /Users/thomas/env_soft/mysql57/datadir:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=123456 -p 3306:3306 -d --restart=always mysql:5.7
```

- --name 指定容器的名称
- -v 关联目录
- -e MYSQL_ROOT_PASSWORD 设置root用户的密码
- -p 指定端口
- --restart=always    指定mysql随着容器的启动而启动

#### 进入容器

```shell
docker exec -it mysql57 bash
```

#### 停止容器:
```shell
docker stop mysql57
```

#### 重新运行容器
````shell
docker start mysql57
````

