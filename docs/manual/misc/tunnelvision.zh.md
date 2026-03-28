---
icon: material/book-lock-open
---

# TunnelVision

TunnelVision 是一种攻击，它利用 DHCP 选项 121 设置更高优先级的路由，  
从而使流量绕过 VPN。

参考：https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2024-3661

## Status

### Android

Android 不处理 DHCP 选项 121，因此不受影响。

### Apple platforms

将 [sing-box 图形客户端](/clients/apple/#download) 更新至 `1.9.0-rc.16` 或更高版本，  
然后在设置中启用 `includeAllNetworks` — `Packet Tunnel`，即可不受影响。

注意：启用 `includeAllNetworks` 后，默认的 TUN 栈会更改为 `gvisor`，  
`system` 和 `mixed` 栈将不可用。

### Linux

将 sing-box 更新至 `1.9.0-rc.16` 或更高版本，由 `auto-route` 生成的规则不受影响。

### Windows

尚无解决方案。

## 解决方法

* 不连接不可信网络
* 通过其他设备中继不可信网络
* 直接忽略
