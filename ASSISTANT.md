# CreditsPlan 助手

CreditsPlan 的 Windows / Mac 桌面客户端：查看 Codex、Claude Code 的本机用量统计，并使用 CreditsPlan 账号访问在线顾问等功能。

## 下载

**[官网下载中心](https://creditsplan.ai/download/)** · 当前版本 v0.1.1

| 平台 | 下载 | 大小 | 发布时间 |
| --- | --- | --- | --- |
| Windows x64 | [EXE 安装包](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.1/CreditsPlan-Assistant-windows-x64-setup.exe) | 12.7 MB | 2026-09-30 |
| Mac · Apple Silicon（M 系列） | [arm64 DMG](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.1/CreditsPlan-Assistant-macos-arm64.dmg) | 17.5 MB | 2026-10-01 |
| Mac · Intel | [x64 DMG](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.1/CreditsPlan-Assistant-macos-x64.dmg) | 17.8 MB | 2026-10-01 |

[查看全部版本和更新说明](https://github.com/CreditsPlan/creditsplan/releases)

Windows 下载 `.exe` 安装包；Mac 下载与芯片对应的 `.dmg`。GitHub 自动提供的 `Source code` 压缩包只包含本下载仓库的说明文件，不是安装程序。

## Mac 安装

1. 在苹果菜单“关于本机”查看芯片：M 系列选择 Apple Silicon，Intel 选择 Intel Mac。
2. 打开 DMG，将 CreditsPlan Assistant 拖入 Applications（应用程序），再从应用程序打开。
3. 当前 Mac 包采用 ad-hoc 临时签名，没有 Apple Developer ID 或 Apple 公证。首次打开可能被系统拦截；核对官方来源后，在“系统设置 → 隐私与安全性”选择“仍要打开”。受管理设备可能限制安装。

最低配置为 macOS 11.0；本次双架构在 macOS 15.7.9 各通过 39 项原生测试、签名验证、DMG 挂载、实际应用启动与本地数据库初始化。尚未在 macOS 11 或普通用户环境完成完整交互流程（登录、真实工具统计、菜单栏、开机启动及升级保留数据）验收。

## Windows 安装

当前安装包未做 Windows 代码签名，Windows 可能显示“未知发布者”或 SmartScreen 提示，部分设备的安全策略可能阻止安装。每个发布版本都附有 SHA-256 校验文件，供核对下载文件。

首次安装可能需要联网安装 Microsoft WebView2。官网登录、顾问和云同步功能需要联网。

当前采用手动更新：新版本发布后，从这里下载新的安装包。

## 本机统计与隐私

助手默认读取当前系统账号下受支持的 Codex、Claude Code 会话日志，提取用量统计并保存在本机；原始日志不会被修改。支持目录为 `~/.codex/sessions`、`~/.codex/archived_sessions` 和 `~/.claude/projects`；Windows 的 `~` 对应用户目录，Mac 对应当前用户主目录。尚不支持自定义日志目录；WSL 与远程会话的兼容性未验证。

云同步默认关闭。登录并主动开启同步后，助手上传用于账号用量分析的统计数据，不上传原始日志或对话正文。可在助手中暂停统计、管理同步及清理数据。

用量和成本分析供参考，不等同于服务商账单。

## 帮助

- 官网：[creditsplan.ai](https://creditsplan.ai)
- 问题反馈：[官网反馈入口](https://creditsplan.ai/feedback/)
- [SHA-256 校验清单](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.1/SHA256SUMS.txt)包含三个安装包和发布材料。
- Windows 许可为 Release 的 `THIRD_PARTY_LICENSES.txt` 与 `THIRD_PARTY_NOTICES.md`；Mac 为 `THIRD_PARTY_MACOS_LICENSES.txt` 与 `THIRD_PARTY_MACOS_NOTICES.md`，也随应用提供。

本仓库用于公开分发安装包和说明，应用源码由独立私有仓库维护。
