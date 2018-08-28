# IPIPChain-Testnet接入指南
欢迎来到 IPIPChain Testnet


## 构建本地环境
```
git clone https://github.com/IPIPChain/eos.git --recursive
```
如果某个存储库没有--recursive标记clone，则可以通过在repo内运行以下命令来检索子模块：
```
git submodule update --init --recursive
```

## 构建
构建EOSIO的简单方法是使用自动构建脚本。
构建将内容放置在eos/build文件夹中。
可执行文件可以在文件eos/build/programs 夹中的子文件夹中找到。

## 自动构建脚本
有一个自动构建脚本，该脚本支持以下操作系统。
1.	Amazon 2017.09 and higher
2.	Centos 7
3.	Fedora 25 and higher (Fedora 27 recommended)
4.	Mint 18
5.	Ubuntu 16.04 LTS (Ubuntu 16.10 recommended)
6.	Ubuntu 18.04 LTS
7.	MacOS Darwin 10.12 and higher (MacOS 10.13.x recommended)

系统要求

•	需要8GB RAM
•	需要20GB磁盘空间

运行构建脚本

从该eos文件夹运行构建脚本。

```
cd eos
./eosio_build.sh
```

安装可执行文件
为了便于合同开发，可以/usr/local使用make install目标将内容安装到文件夹中。该步骤从该build文件夹运行。安装需要足够的权限，因此我们使用该sudo命令make install。

```
CD build
sudo make install
```

## Docker
Docker上简单快速的EOSIO设置也是可用的。
安装依赖关系
•	需要Docker Docker 17.05或更高版本
构建EOSIO映像

```
git clone https://github.com/IPIPChain/eos.git --recursive
$ cd eos / Docker
$ docker build -t eosio / eos
```
仅启动nodeos docker容器
```
$ docker run --name nodeos -p 8888：8888 -p 9876：9876 -t eosio / eos nodeosd.sh arg1 arg2
```

您可以直接将主机目录挂载到容器中
```
$ docker run --name nodeos -v / path-to-data-dir：/ opt / eos / bin / data-dir -p 8888：8888 -p 9876：9876 -t eosio / eos nodeosd.sh arg1 arg2
```

获取区块链信息
```
$ curlhttp://47.92.0.237:8855/v1/chain/get_info
```


## 依赖
- [Docker](https://docs.docker.com) Docker版本 >= 17.05
- [docker-compose](https://docs.docker.com/compose/) 版本 >= 1.10.0



## 链信息

```
{
  "chain_id": "493b4b275a7b387cd2e16ab0b53aa59e53ff53fa7d4474ed640d25b70efdca13"
}
```

## P2P 节点列表

```
p2p-peer-address=47.92.97.56:9109
p2p-peer-address=47.92.0.237:8866

```


## HTTP API 节点列表

```
http://47.92.0.237:8855/v1/chain/get_info

```

