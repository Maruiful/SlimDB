# SlimDB

SlimDB 是一个用 Java 实现的轻量级关系型数据库，实现了现代数据库的核心特性。

## ✨ 主要特性

- 🔒 **数据可靠性**：完善的数据恢复机制
- 🔐 **并发控制**：基于两段锁协议（2PL）的可串行化调度
- 📦 **MVCC**：多版本并发控制
- 🎯 **事务隔离**：支持读提交（RC）和可重复读（RR）两种隔离级别
- 💀 **死锁处理**：自动检测和处理死锁
- 📋 **表和字段管理**：灵活的数据结构定义
- 🔍 **SQL 解析**：支持常用 SQL 语句
- 🌐 **客户端-服务器架构**：基于 Socket 的通信

## 🚀 快速开始

### 环境要求

- JDK 8 或更高版本
- Maven 3.x

### 编译项目

```shell
mvn compile
```

### 创建数据库

```shell
mvn exec:java -Dexec.mainClass="top.maruiful.slimdb.backend.Launcher" -Dexec.args="-create /tmp/mydb"
```

### 启动服务器

```shell
mvn exec:java -Dexec.mainClass="top.maruiful.slimdb.backend.Launcher" -Dexec.args="-open /tmp/mydb"
```

数据库服务将在本地 9999 端口启动。

### 启动客户端

打开新终端，执行：

```shell
mvn exec:java -Dexec.mainClass="top.maruiful.slimdb.client.Launcher"
```

现在可以输入 SQL 语句进行交互了！
