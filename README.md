# IPIPChain-Testnet接入指南
欢迎来到 IPIPChain Testnet


二、构建本地环境
```
git clone https://github.com/IPIPChain/eos.git --recursive
```
如果某个存储库没有--recursive标记clone，则可以通过在repo内运行以下命令来检索子模块：
```
git submodule update --init --recursive
```
##依赖
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

