## Demo10 : 容器進階管理
除了以上的基本管理方式(啟動、停止、重新啟動、刪除)外，筆者還整理了一些好用的管理指令供使用者使用。例如，當你容器很多，且需全部刪除時，不必一個一個慢慢刪除。在這裡我們教你一些進階的管理方式，讓你更輕鬆且有效率的對容器進行操作。

## 前置
我們需先確認有一個以上的容器處於執行狀態，我們可以透過 `docker ps` 檢視。

```
$ docker ps
```

```
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
72c12f3887e3        ubuntu:14.04        "bash"              19 minutes ago      Up 19 minutes                           desperate_lovelace

```

與確認有一個以上的映像檔從在於環境中，

```
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
ubuntu              14.04               4d44acee901c        7 days ago          187.9 MB
hello-world         latest              c54a2cc56cbb        4 months ago        1.848 kB
```

## 實作

### 刪除多個映像檔

```
$ docker rmi $(docker images -a -q)
```

### 刪除多個容器

```
$ docker rm $(docker ps -a -q)
```

### 刪除無標籤映像檔

```
$ docker rmi $(docker images -q --filter="dangling=true")
```

### 刪除所有狀態為 Exited 的容器

```
$ docker rm $(docker ps -a | grep Exited | awk '{print $1}')
```

### 停止並刪除所有容器

```
docker rm -f $(docker ps -a -q)
```

### 刪除所有指定映像檔所建立的容器

```
docker rm `docker ps -a | grep <image_name>:<image_version> | cut -f1 -d" "`
```

### 刪除所有映像檔

```
$ docker rmi $(docker ps -a -q)
```

## 結果

無