### Go 学习笔记

#### Go初始化
> 进入Go项目所在的文件夹
> 执行```go mod init godemo
> 其中godemo是go项目文件夹名称
> 此时文件夹中会生成一个go.mod文件，这个文件记录的是go的所有项目依赖，类似于package.json

#### 安装依赖
> 在Go项目所在的文件夹，执行```go get github.com/json-iterator/go
> github.com/json-iterator/go是项目依赖，在go的文件中，可以直接通过 import ("github.com/json-iterator/go") 引入依赖
> 安装的时候可能会报下面的错误
> go get: module github.com/json-iterator/go: Get "https://proxy.golang.org/github.com/json-iterator/go/@v/list": dial tcp 172.217.160.81:443: connectex: A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond.
> 则需要设置CDN代理

#### 代理设置
> 国内网络安装需要设置国内镜像源
> go env -w GOPROXY=https://goproxy.cn