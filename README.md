# Overview
Based on protobuf's c distributed network communication framework, this project uses zookeeper as a service middleware, which is responsible for solving problems such as service release and invocation, message sequence and deserialization, and network packet sending and receiving in distributed service deployment, so that it can provide highly concurrent remote function call services. Allows users to focus on the business.

## operating environment

Ubuntu 22.04 LTS

## Library

1. Install tools
```shell
sudo apt-get install -y wget cmake build-essential unzip
```

2. Muduo Installation
Muduo is an efficient network library based on multithreaded Epoll mode, which is responsible for the network communication of data flow.

- Reference：[Mudo](https://blog.csdn.net/QIANGWEIYUAN/article/details/89023980)

3. Zookeeper Installation
Zookeeper is responsible for service registration and discovery, and dynamically records the IP address and port number of the service, so that the caller can quickly find the target service.


* Zookeeper：
```shell
sudo apt install zookeeperd
```
* Zookeeper Dev library：
```shell
sudo apt install libzookeeper-mt-dev
```
4. Protobuf
Protobuf is responsible for registering RPC methods, serializing and deserializing data.
Compared to XML and JSON, Protobuf is binary storage, which is more efficient.
Local version: 3.12.4
It can be installed directly on Ubuntu 22:
```shell
sudo apt-get install protobuf-compiler libprotobuf-dev
```
5. boost
```shell
sudo apt-get install -y libboost-all-dev
```

6. Glog
Glog is an efficient asynchronous log library for logging debug and error logs during framework runtime.
```shell
sudo apt-get install libgoogle-glog-dev libgflags-dev
```
