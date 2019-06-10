+ build new version
```
docker build -t serverAddress/yourDir/mitchell_python:1.0.1 .
```
+ push
```
docker push serverAddress/yourDir/mitchell_python:1.0.1
```
+ pull
```
docker pull serverAddress/yourDir/mitchell_python:1.0.0
```

+ login 有符号前面可能需要添加转义字符
docker login --username=guest -p \!pwd serverAddress

+ run
```
docker run -d -p 8000:8080 serverAddress/yourDir/mitchell_python:1.0.1
```

+ ps 查看进程
```
docker ps
```

+ kill 杀死进程
```

docker kill (CONTAINER ID)
```
+ images 查看镜像
```
docker images 
```

+ 删除容器
```
docker rm container
```

+ 删除镜像
```
docker rmi image
```

+ 端口映射
```
p1：host 端口
p2：docker 实例端口
docker run -p p1:p2 -d tomcat:8.0
docker run -p 8000:8080 -d tomcat:8.0
```

+ 目录挂载
```
dir1：host 机目录
dir2：容器目录
docker run -v dir1:dir2
```

