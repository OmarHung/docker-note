# docker-note
Docker學習紀錄

Docker Desktop https://www.docker.com/products/docker-desktop

# 指令
查看images 
```cmd
1. docker images
2. docker image ls
```
查看版本 
1. docker --version

從Docker Hub取得image
1. docker pull IMAGE_NAME

刪除image 
1. docker rmi IMAGE_NAME
2. docker image rm IMAGE_NAME

刪除container 
1. docker rm CONTAINER_NAME|CONTAINER_ID
2. docker container rm CONTAINER_NAME|CONTAINER_ID

查看目前運行的container 
1. docker ps
2. docker container ls

查看目前全部的container(包含停止狀態的container）
1. docker ps -a
2. docker container ls -a

新建並啟動container 
1. docker run -d -p 80:80 --name my_image ubuntu
-d 代表在 Detached（ 背景 ）執行，如不加 -d，預設會 foreground ( 前景 ) 執行
-p 代表將本機的 80 port 的所有流量轉發到 container 中的 80 port
--name 設定 container 的名稱

啟動container
1. docker start CONTAINER_NAME|CONTAINER_ID

回到運行中的container
1. docker exec -it CONTAINER_NAME|CONTAINER_ID