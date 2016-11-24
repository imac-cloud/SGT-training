## Demo08 : 進入 Ubuntu
我們當前已經啟動了一個 Ubuntu 的容器，下一步你應該想了解如何進入容器內進行操作吧！在這裡我們教你如何進入已存在的 Ubuntu 容器中。

## 前置
我們需先使用 `docker ps` 確認當前執行中的容器列表中存在 Ubuntu 的容器。

```
$ docker ps
```

```
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
72c12f3887e3        ubuntu:14.04        "bash"              9 seconds ago       Up 2 seconds                            desperate_lovelace

```


## 實作
接著，使用 `docker exec -ti <Container_id>` bash 進入 Ubuntu 作業系統中。

```
docker exec -ti 72c12f3887e3 bash
```

> 在這裡使用者必須注意 <Container_id> 是由查詢指令所回傳的結果所帶入的參數，這裡若你與筆者輸入相同的 Container ID 是無法使用的！

若進入成功，你可以看到如結果的畫面。最後你就可以依照需求自行安裝相依套件或佈署應用環境。

## 結果

```
root@72c12f3887e3:/#
```