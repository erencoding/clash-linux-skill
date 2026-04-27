# Clash for Linux Skill

🌐 OpenClaw skill for managing Clash proxy on Linux systems.

## Overview

This skill provides commands to control [Clash for Linux](https://github.com/wnlen/clash-for-linux), including:
- Proxy on/off
- Node selection
- Subscription management
- Status checking

## Usage

When user mentions: `Clash`, `代理`, `翻墙`, `开启代理`, `关闭代理`, `切换节点`, `Clash订阅`

The skill will:
1. Check if Clash is installed
2. Auto-install if not found
3. Execute the requested operation

## Commands

```bash
clashon              # 开启代理
clashoff             # 关闭代理
clashctl status      # 查看状态
clashctl select      # 交互式选择节点
clashctl add         # 添加订阅
clashctl use <name>  # 切换订阅
clashctl ls          # 查看订阅列表
clashctl secret      # 查看/设置密钥
clashctl tun on|off  # Tun 模式
clashctl boot on|off # 开机自启
clashctl doctor      # 诊断
clashctl log         # 查看日志
clashctl upgrade     # 升级内核
```

## Requirements

- Linux system (VPS, WSL, OpenWrt, Debian/Ubuntu, etc.)
- Root/sudo access for installation

## Installation

This skill auto-installs Clash for Linux when needed via:

```bash
git clone --branch master --depth 1 \
  https://ghfast.top/https://github.com/wnlen/clash-for-linux.git \
  /tmp/clash-for-linux
cd /tmp/clash-for-linux && bash install.sh
```

## Credit

- [Clash for Linux](https://github.com/wnlen/clash-for-linux) by wnlen
- Built for [OpenClaw](https://openclaw.ai/)
