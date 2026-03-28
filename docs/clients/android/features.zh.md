# :material-decagram: 功能

#### UI 选项

* 在通知栏显示实时网络速度

#### 服务

SFA 允许你通过前台服务（ForegroundService）或 VpnService（当需要 TUN 时）运行 sing-box。

#### TUN

SFA 通过 Android VpnService 提供无需特权的 TUN 实现。

| TUN inbound option            | Available        | Note               |
| ----------------------------- | ---------------- | ------------------ |
| `interface_name`              | :material-close: | Managed by Android |
| `inet4_address`               | :material-check: | /                  |
| `inet6_address`               | :material-check: | /                  |
| `mtu`                         | :material-check: | /                  |
| `gso`                         | :material-close: | No permission      |
| `auto_route`                  | :material-check: | /                  |
| `strict_route`                | :material-close: | Not implemented    |
| `inet4_route_address`         | :material-check: | /                  |
| `inet6_route_address`         | :material-check: | /                  |
| `inet4_route_exclude_address` | :material-check: | /                  |
| `inet6_route_exclude_address` | :material-check: | /                  |
| `endpoint_independent_nat`    | :material-check: | /                  |
| `stack`                       | :material-check: | /                  |
| `include_interface`           | :material-close: | No permission      |
| `exclude_interface`           | :material-close: | No permission      |
| `include_uid`                 | :material-close: | No permission      |
| `exclude_uid`                 | :material-close: | No permission      |
| `include_android_user`        | :material-close: | No permission      |
| `include_package`             | :material-check: | /                  |
| `exclude_package`             | :material-check: | /                  |
| `platform`                    | :material-check: | /                  |

| Route/DNS rule option | Available        | Note                              |
| --------------------- | ---------------- | --------------------------------- |
| `process_name`        | :material-close: | No permission                     |
| `process_path`        | :material-close: | No permission                     |
| `process_path_regex`  | :material-close: | No permission                     |
| `package_name`        | :material-check: | /                                 |
| `user`                | :material-close: | Use `package_name` instead        |
| `user_id`             | :material-close: | Use `package_name` instead        |
| `wifi_ssid`           | :material-check: | Fine location permission required |
| `wifi_bssid`          | :material-check: | Fine location permission required |

### 覆盖

用平台特定的值覆盖配置文件中的配置项。

#### 单应用代理

SFA 允许你在图形界面中选择需要代理或绕过的 Android 应用列表，以覆盖 include_package 和 exclude_package 配置项。

特别地，选择器还提供“国内应用”扫描功能，为中国用户提供了极佳的体验，可绕过不需要代理的应用。具体来说，通过 dex 类路径等方式扫描国内应用或 SDK 特征，几乎不会漏报。

### 其他

* 工作目录位于 /sdcard/Android/data/io.nekohasekai.sfa/files（外部文件目录）
* 崩溃日志位于 $working_directory/stderr.log
