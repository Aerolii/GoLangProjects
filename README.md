# Golang 项目合集

## Go 语言开发环境搭建

### Windows 平台安装 Go

- 下载`Go`安装包并安装，例如：`c:/go`。
- 添加`Go`系统环境变量，例如：`c:\go\bin`添加到系统环境变量。命令后输入`go version`查看版本信息，输出结果如下所示

```shell
  go version go1.16.6 windows/amd64
```

#### 配置`Go`环境

命令行输入：`go env` 查看环境配置。

由于目前都使用`go mode`管理项目，因此`env:GO111MODULE="on`需要设置为`on`。

> `GO111MODUILE`是指1.11版本之后使用模块化管理，不再依赖GOPATH。

### MacOS 安装 Go

- 下载`Go`安装包并安装，安装包默认安装到`/usr/local/go`。
- 添加`Go`系统环境变量

```shell
vim ~/.bash_profile
```

#### 配置环境变量：

```shell
# Golang
export GOROOT=/usr/local/go
export PATH=$PATH:$GOROOT/bin
export GOPATH=$HOME/GOlang # 工作区目录

export GO111MODULE=on # module
export GOPROXY=https://goproxy.cn # 代理
    
# Golang END
```

#### 开启`Go Module`

```shell
go env -w GO111MODULE=on
```

## Golang workspaces设置

Go 版本 >= 1.18时，在设置了`GOPATH`路径的工作区文件夹内，如果使用`go mod init project_name`初始化时，vscode 会报错，提示`gopls`必须是根路径，因此需要使用以下命令初始化工作区：

```shell
cd $WORK # 工作区路径
go work init
go work use tools tools/gopls
```

## [Golang language](./GoLangStudyNote/)

Golang 基础语法学习笔记。