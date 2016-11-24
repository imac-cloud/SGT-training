## Demo05 : 啟動容器(Container)
我們已經學會下載映像檔(Image)，也了解如何檢視目前以存在的映像檔，接著我們要啟動相對應的服務，在 Docker 中我們稱服務為容器(Container)。在這裡我們教你如何將現有的 `hello-world` 映像檔啟動成 `hello-world` 容器。

## 前置
首先，需先使用 `docker pull hello-world` 取得映像檔。

```
$ docker pull hello-world
```

## 實作
接著，我們透過 `docker run hello-world` 將映像檔啟動成容器。

```
$ docker run hello-world
```

## 結果

```
Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker Hub account:
 https://hub.docker.com

For more examples and ideas, visit:
 https://docs.docker.com/engine/userguide/
```