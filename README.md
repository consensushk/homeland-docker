Homeland Docker
-----------------

[Homeland](http://gethomeland.com) 基于 Docker 的自动化部署方案。

## 系统需求

- Linux Server [4 Core CPU, 4G Memory, 50G Disk, 64 位] - _建议 Ubuntu Server 14.04_
- [Docker](https://www.docker.com/), [Docker Compose](https://docs.docker.com/compose/)
- [Aliyun OSS](https://www.aliyun.com/product/oss) 或 [UpYun](https://www.upyun.com) 用于文件存储。

## 使用说明

```
  Command	Desc
  make install	首次安装，创建数据库
  make install_ssl	安装并申请 SSL 证书
  make update	更新应用程序，当 consensushk/homeland image 版本变化，需要合并数据库、编译 Assets
  make start	启动所有服务，将会自动启动所有的服务
  make stop	停止所有服务
  make restart	硬重启服务
  make status	查看服务状态
  make console	进入 Rails 控制台
  make stop-all	停止所有服务，包括数据库
  make reindex	重建搜索索引
```

http://gethomeland.com/install/
