## Demo07 : 啟動一個 Ubuntu
接著我們實作進階的練習，啟動容器也可以加入參數，讓容器與使用者可以進行互動。在這裡我們教你如何使用映像檔(Image)，啟動一個 Ubuntu 14.04 的容器(Container)。

## 前置
無

## 實作
首先，我們先下載 `ubuntu:14.04` 的映像檔。

```
$ docker pull ubuntu:14.04
```

> 我們可以使用 `docker pull <image_name>:<image_version>` 指定下載映像檔的版本，若沒有指定系統預設下載 `latest` 版本。

接著，我們使用啟動指令並且加入參數執行這個映像檔。

```
$ docker run -tid ubuntu:14.04 bash
```

> -tid 表示我們要將容器執行在背景模式下，並且開啟互動模式
> 
> bash 表示分配偽終端執行 bash 指令提供使用者互動

最後，我們可以由當前容器列表中發現 `ubuntu:14.04` 容器。

```
$ docker ps
```


## 結果

```
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
72c12f3887e3        ubuntu:14.04        "bash"              9 seconds ago       Up 2 seconds                            desperate_lovelace
```