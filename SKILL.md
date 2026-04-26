---
name: clash-linux
description: Manage Clash proxy on Linux systems. Automatically installs if not found. Use when user wants to control Clash (clash-for-linux), turn proxy on/off, select nodes, manage subscriptions, or check Clash status.
version: "1.1"
author: Judy (朱迪)
license: MIT
---

# Clash for Linux Skill

Manages Clash proxy on Linux. Works on VPS, WSL, OpenWrt, Debian/Ubuntu, etc.

## Usage Keywords

```
Clash
代理
翻墙
开启代理
关闭代理
切换节点
Clash订阅
clashforlinux
```

## Workflow

### Step 1: Check if Clash is Installed

```bash
which clashon 2>/dev/null || which clashctl 2>/dev/null
```

If NOT installed → auto install first.

### Step 2: Auto Install (if not found)

```bash
# Clone repository
git clone --branch master --depth 1 https://ghfast.top/https://github.com/wnlen/clash-for-linux.git /tmp/clash-for-linux

# Run installer
cd /tmp/clash-for-linux && bash install.sh

# Verify
clashctl status
```

### Step 3: Check Status

```bash
clashctl status
```

## Core Commands

### Proxy Control
```bash
clashon    # 开启代理
clashoff   # 关闭代理
```

### Node & Subscription
```bash
clashctl select        # 交互式选择节点（输入策略组编号 → 再输入节点编号）
clashctl add           # 添加订阅
clashctl use <name>    # 切换主订阅
clashctl ls            # 查看订阅列表
```

### Security
```bash
clashctl secret              # 查看当前密钥
clashctl secret <新密钥>      # 设置密钥
```

### Advanced
```bash
clashctl tun on|off|status   # Tun 模式
clashctl boot on|off|status   # 开机自启
clashctl mixin                # Mixin 配置
clashctl doctor               # 诊断面板
clashctl log                  # 查看日志
clashctl upgrade              # 升级内核
clashctl update              # 更新项目
```

### Console
```bash
clashui   # 查看 Web 控制台地址和密钥
```

## Notes
- Installation: `git clone + bash install.sh`
- Web console default port: 9090
- Default proxy port: 7890
