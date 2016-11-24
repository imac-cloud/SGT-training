## Demo04 : 檢視目前已下載的映像檔
我們已經學會取得映像檔(Image)後，你會許會想知道我們怎麼知道剛才下載的映像檔是否有成功。在這裡我們教你如何透過指令查詢目前 Docker 環境上以存在的映像檔列表。

## 前置
首先，需先使用 `docker pull hello-world` 取得映像檔。

```
$ docker pull hello-world
```

## 實作
接著，我們透過 `docker images` 檢視當前已經存在的映像檔。

```
$ docker images
```

## 結果

```
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
hello-world         latest              c54a2cc56cbb        4 months ago        1.848 kB
```