# octorpki_gortr

## Overview
octorpkiとgortrをコンテナ稼働させるためのcompose file  

[cloudflare/octorpki](https://hub.docker.com/r/cloudflare/octorpki)  
[cloudflare/gortr](https://hub.docker.com/r/cloudflare/gortr)  

## Setup
docker-compose.yamlを編集します。  

`(Your Internal|External Address)`を環境に合わせて変更します  
.envで定義し変数化しても問題ないです  

その他利用ポートが重複する場合は適宜変更  

## Usage
Setupに記載した編集を行ったら起動します
```bash
$ docker-compose build
$ docker-compose up -d
```

routerからgortrへのアクセスポートは8282です。
必要に応じてホスト側でアクセス許可をしてください

## Requirement
OS: Ubuntu 22.04.2 LTS  
docker: 
```bash
$ docker version
Client: Docker Engine - Community
 Version:           23.0.1
 API version:       1.42
 Go version:        go1.19.5
 Git commit:        a5ee5b1
 Built:             Thu Feb  9 19:47:01 2023
 OS/Arch:           linux/amd64
 Context:           default

Server: Docker Engine - Community
 Engine:
  Version:          23.0.1
  API version:      1.42 (minimum version 1.12)
  Go version:       go1.19.5
  Git commit:       bc3805a
  Built:            Thu Feb  9 19:47:01 2023
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.6.18
  GitCommit:        2456e983eb9e37e47538f59ea18f2043c9a73640
 runc:
  Version:          1.1.4
  GitCommit:        v1.1.4-0-g5fd4c4d
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0
```

docker compose:  
```bash
$ docker compose version
Docker Compose version v2.16.0
```
