## Demo01 : 檢視 Docker 版本
使用者在操作 Docker 時，若系統發生錯誤，可能在處理當前問題時，需要了解 Docker 環境的版本。在這裡我們要學習如何透過指令，取得我們當前環境的版本號。 

## 前置
無

## 實作
開啟終端機，並輸入 `docker version` 即可檢視當前 Docker 環境版本。

```
$ docker version
```

## 結果

```
Client:
 Version:      1.12.3
 API version:  1.24
 Go version:   go1.6.3
 Git commit:   6b644ec
 Built:        Wed Oct 26 23:26:11 2016
 OS/Arch:      darwin/amd64

Server:
 Version:      1.12.3
 API version:  1.24
 Go version:   go1.6.3
 Git commit:   6b644ec
 Built:        Wed Oct 26 23:26:11 2016
 OS/Arch:      linux/amd64
```