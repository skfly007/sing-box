# :material-decagram: Features

#### UI options

* 始终开启
* 包含所有网络（为局域网和蜂窝网络服务的流量代理）
* （Apple tvOS）从 iPhone/iPad 导入配置文件

#### Service

SFI/SFM/SFT 允许你通过带有应用扩展或系统扩展的 NetworkExtension 运行 sing-box。

#### TUN

SFI/SFM/SFT 通过 NetworkExtension 提供无需特权的 TUN 实现。

| TUN inbound option            | Available        | Note              |
| ----------------------------- | ---------------- | ----------------- |
| `interface_name`              | :material-close:️ | Managed by Darwin |
| `inet4_address`               | :material-check: | /                 |
| `inet6_address`               | :material-check: | /                 |
| `mtu`                         | :material-check: | /                 |
| `gso`                         | :material-close: | Not implemented   |
| `auto_route`                  | :material-check: | /                 |
| `strict_route`                | :material-close:️ | Not implemented   |
| `inet4_route_address`         | :material-check: | /                 |
| `inet6_route_address`         | :material-check: | /                 |
| `inet4_route_exclude_address` | :material-check: | /                 |
| `inet6_route_exclude_address` | :material-check: | /                 |
| `endpoint_independent_nat`    | :material-check: | /                 |
| `stack`                       | :material-check: | /                 |
| `include_interface`           | :material-close:️ | Not implemented   |
| `exclude_interface`           | :material-close:️ | Not implemented   |
| `include_uid`                 | :material-close:️ | Not implemented   |
| `exclude_uid`                 | :material-close:️ | Not implemented   |
| `include_android_user`        | :material-close:️ | Not implemented   |
| `include_package`             | :material-close:️ | Not implemented   |
| `exclude_package`             | :material-close:️ | Not implemented   |
| `platform`                    | :material-check: | /                 |

| Route/DNS rule option | Available        | Note                  |
| --------------------- | ---------------- | --------------------- |
| `process_name`        | :material-close: | No permission         |
| `process_path`        | :material-close: | No permission         |
| `process_path_regex`  | :material-close: | No permission         |
| `package_name`        | :material-close: | /                     |
| `user`                | :material-close: | No permission         |
| `user_id`             | :material-close: | No permission         |
| `wifi_ssid`           | :material-alert: | Only supported on iOS |
| `wifi_bssid`          | :material-alert: | Only supported on iOS |

### Chore

* 崩溃日志位于 `设置` -> `查看服务日志`
