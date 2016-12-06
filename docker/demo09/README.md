## Demo09 : 容器基本管理
到目前我們已經學會如何下載映像檔(Image)、啟動容器(Container)、進入容器，接著我們要學習如何管理容器。在這裡我們教你如何針對容器進行啟動、停止、重新啟動、刪除...等操作。

## 前置
我們需先確認有一個以上的容器處於執行狀態，我們可以透過 `docker ps -a` 檢視所有容器目前的狀態(status)。

```
$ docker ps -a
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

### 停止(Stop)
首先，我們學習如何停止目前正在執行的容器。以下使用的 Container ID 使用者接需自行更改。

```
docker stop 72c12f3887e3
```

### 啟動(Start)
接著，我們操作啟動指令。

```
docker start 72c12f3887e3
```

### 重新啟動(Restart)
重新啟動除了可以使用以下方法外，也可使用暫停與啟動達到同樣的效果。

```
docker restart 72c12f3887e3
```

### 刪除(Delete)容器
最後，我們學習如何將已存在的容器刪除。

```
docker rm 72c12f3887e3
```

> 這裡使用者必須注意，刪除動作必須在容易處於暫停狀態才能成功被執行！

### 刪除映像檔

```
docker rmi 4d44acee901c
```

> 這裡我們可以透過 Container ID 或映像檔名稱進行刪除，並且需注意若有兩個以上的映像檔名稱存在，表示該映像檔存在兩個不同版本以上，則刪除需如： `docker rmi ubuntu:14.04` 附加版本號。


## 結果

無