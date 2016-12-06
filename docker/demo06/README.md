## Demo06 : 列出容器列表
我們已經了解如何從一個映像檔(Image)啟動一個容器(Container)，現在你可能會有個疑問，我們該從哪裡看到正在執行的容器？在這裡我們教你如何使用查詢容器指令，列出以存在的容器。

## 前置
我們透過 `docker run hello-world` 將映像檔啟動成容器。

```
$ docker run hello-world
```

## 實作

這裡我們介紹兩個方式，首先，我們使用 `docker ps` 查詢目前正在執行中的容器。

```
$ docker ps
```

另一個方式，我們也可以使用 `docker ps -a` 查詢所有容器(包含：正在執行、已停止)。

```
$ docker ps -a
```

## 結果

```
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                         PORTS               NAMES
fabc57c5a64e        hello-world         "/hello"            About an hour ago   Exited (0) About an hour ago                       goofy_mayer
```