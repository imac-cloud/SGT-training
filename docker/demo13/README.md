## Demo13 : 容器打包
你是否好奇 Docker Hub 上的映像檔(Image)是如何打包的呢？在這裡我們要教你如何將現有的容器(Container)打包成映像檔。

## 前置
擁有一個以上正在執行的容器，也可以透過前一個練習(Demo12)所建置的簡易網站進行打包。

> 建議使用者實作此練習時，將現有的映像檔進行內容修改，這樣一來就可以觀察出其中的差異。

## 實作

首先，使用以下指令給予新的映像檔一個簡易的訊息並打包。

```
$ docker commit -m "first version" 6a9c5e18fe93
```

> 指令格式如： docker commit -m "訊息內容" <容器 ID>

接下來，你會在映像檔列表中發現一個尚未擁有名稱與版本號的映像檔，如下：

```
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
<none>              <none>              4a31dfdcb4f2        10 seconds ago      220.2 MB
nginx               latest              abf312888d13        7 days ago          181.5 MB
```

接著，我們透過下列指令給予他一個名稱與版本號。

```
$ docker tag 4a31dfdcb4f2 cijie/web:1.0.0
```

> 指令格式如： docker tag <映像檔 ID> 使用者名稱/新映像檔名稱:版本號
> 注意，若未給予映像檔版本號，則系統預設給予 latest 版本號。

## 結果

最後結果如下。

```
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
cijie/web           1.0.0               4a31dfdcb4f2        2 minutes ago       220.2 MB
nginx               latest              abf312888d13        7 days ago          181.5 MB
```
