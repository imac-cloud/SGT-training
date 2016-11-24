## Demo02 : 檢視 Docker 相關資訊
使用者除了能了解當前的使用的 Docker 版本，也可以透過指令檢視目前環境上的狀態與資訊。在這裡我們教你如何取得當前 Docker 環境所包含容器(Container)的執行中、停止或暫停的數量、映像檔(Image)的數量、記憶體(Memory)...等等資訊。

## 前置
無

## 實作
開啟終端機，並輸入 `docker info` 即可檢視當前 Docker 的相關資訊。

```
$ docker info
```

## 結果

```
Containers: 0
 Running: 0
 Paused: 0
 Stopped: 0
Images: 0
Server Version: 1.12.3
Storage Driver: aufs
 Root Dir: /var/lib/docker/aufs
 Backing Filesystem: extfs
 Dirs: 0
 Dirperm1 Supported: true
Logging Driver: json-file
Cgroup Driver: cgroupfs
Plugins:
 Volume: local
 Network: bridge overlay null host
Swarm: inactive
Runtimes: runc
Default Runtime: runc
Security Options: seccomp
Kernel Version: 4.4.27-moby
Operating System: Alpine Linux v3.4
OSType: linux
Architecture: x86_64
CPUs: 2
Total Memory: 1.951 GiB
Name: moby
ID: 5GFO:DDYM:TJAZ:LVGL:3MAP:MLZG:CBLB:BZKG:BLLB:JWJ6:F7VN:HYPJ
Docker Root Dir: /var/lib/docker
Debug Mode (client): false
Debug Mode (server): true
 File Descriptors: 15
 Goroutines: 27
 System Time: 2016-11-24T06:20:46.96524856Z
 EventsListeners: 1
No Proxy: *.local, 169.254/16
Username: cijie
Registry: https://index.docker.io/v1/
WARNING: No kernel memory limit support
Insecure Registries:
 127.0.0.0/8```