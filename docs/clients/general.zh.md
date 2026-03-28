---
icon: material/pencil-ruler
---

# 通用

描述并解释 sing-box 图形客户端统一实现的功能。

### 配置文件

配置文件描述 sing-box 的配置文件及其状态。

#### 本地

* 本地配置文件表示本地 sing-box 配置，状态最小化
* 图形客户端必须提供编辑器以修改配置内容

#### iCloud（在 iOS 和 macOS 上）

* iCloud 配置文件表示以 iCloud 作为更新源的远程 sing-box 配置
* 配置文件存储在 iCloud 下的 sing-box 文件夹中
* 图形客户端必须提供编辑器以修改配置内容

#### 远程

* 远程配置文件表示以 URL 作为更新源的远程 sing-box 配置
* 图形客户端应提供配置内容查看器
* 图形客户端必须实现自动配置文件更新（默认间隔为 60 分钟）以及 HTTP Basic 授权

同时，图形客户端必须提供通过特定 URL Scheme 导入远程配置文件的支持。URL 定义如下：

```
sing-box://import-remote-profile?url=urlEncodedURL#urlEncodedName
```

### 仪表板

当 sing-box 服务运行时，图形客户端应提供仪表板接口以管理服务。

#### 状态

仪表板应显示状态信息，例如内存、连接和流量。

#### 模式

当配置至少使用两个 clash_mode 值时，仪表板应提供模式选择器以进行切换。

#### 分组

当配置包含分组出站（特别是 Selector 或 URLTest）时，仪表板应提供分组选择器用于状态显示或切换。

### 其他

#### 核心

图形客户端应提供Core区域：

* 显示当前 sing-box 版本
* 提供按钮以清理工作目录
* 提供内存限制开关