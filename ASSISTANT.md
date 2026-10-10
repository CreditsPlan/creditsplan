# CreditsPlan 助手

CreditsPlan 的 Windows / Mac 桌面客户端：查看 Codex、Claude Code 的本机用量统计，并使用 CreditsPlan 账号访问在线顾问等功能。

## 下载

**[官网下载中心](https://creditsplan.ai/download/)** · Mac v0.1.11 正式签名版；Windows 下载条目保持原版本

| 平台 | 下载 | 大小 | 发布时间 |
| --- | --- | --- | --- |
| Windows x64 | [EXE 安装包](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.7/CreditsPlan-Assistant-windows-x64-setup.exe) | 14.7 MB | 2026-10-06 |
| Mac · Apple Silicon（M 系列） | [arm64 DMG](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.11-macos-signed.1/CreditsPlan-Assistant-macos-arm64.dmg) | 19.2 MB | 2026-10-10 |

[查看全部版本和更新说明](https://github.com/CreditsPlan/creditsplan/releases)

Windows 下载 `.exe` 安装包；Mac M 系列芯片下载 Apple Silicon 的 `.dmg`。GitHub 自动提供的 `Source code` 压缩包只包含本下载仓库的说明文件，不是安装程序。

## Mac 安装

1. 在苹果菜单“关于本机”查看芯片：仅支持 Apple Silicon（M 系列），**不支持 Intel Mac**。
2. 从本页或官网下载 DMG，核对 [Mac SHA-256 校验清单](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.11-macos-signed.1/SHA256SUMS.txt)，将“CreditsPlan 助手”拖入 Applications（应用程序），再从应用程序打开。
3. App 与 DMG 均使用 `Developer ID Application: Yonglin Xu (RXNQMB7WHQ)` 正式签名，分别通过 Apple 公证并附加票据。首次启动可能出现正常的“从互联网下载的应用”确认，核对来源后点击“打开”。若签名验证失败，请停止安装并反馈错误，不要关闭系统安全保护。

系统要求 macOS 11.0 或更高版本；已在 macOS 15.3.1 验证签名、公证、Gatekeeper、DMG 挂载安装、应用启动及独立 HOME 数据库初始化。完整业务交互和所有系统版本的兼容性尚未逐项验收。

详细信息见 [Mac 安装说明](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.11-macos-signed.1/INSTALL-macos.md) 和 [平台发布清单](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.11-macos-signed.1/release-manifest-macos-arm64.json)。本次为 0.1.11 的签名构建修订，请手动下载安装；当前客户端不会将该修订标签识别为新版本。

## Windows 安装

当前安装包未做 Windows 代码签名，Windows 可能显示“未知发布者”或 SmartScreen 提示，部分设备的安全策略可能阻止安装。每个发布版本都附有 SHA-256 校验文件，供核对下载文件。

首次安装可能需要联网安装 Microsoft WebView2。官网登录、顾问和云同步功能需要联网。

当前采用手动更新：新版本发布后，从这里下载新的安装包。

## 启动器支持范围

Windows 当前自动发现 Cursor，其他受支持桌面工具需要手动添加。Mac 启动器尚未实现，应用会保留“不支持”的限制。

## 本机统计与隐私

助手默认读取当前系统账号下受支持的 Codex、Claude Code 会话日志，提取用量统计并保存在本机；原始日志不会被修改。支持目录为 `~/.codex/sessions`、`~/.codex/archived_sessions` 和 `~/.claude/projects`；Windows 的 `~` 对应用户目录，Mac 对应当前用户主目录。尚不支持自定义日志目录；WSL 与远程会话的兼容性未验证。

云同步默认关闭。登录并主动开启同步后，助手上传用于账号用量分析的统计数据，不上传原始日志或对话正文。可在助手中暂停统计、管理同步及清理数据。

用量和成本分析供参考，不等同于服务商账单。

## 帮助

- 官网：[creditsplan.ai](https://creditsplan.ai)
- 问题反馈：[官网反馈入口](https://creditsplan.ai/feedback/)
- [Windows 原版本校验清单](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.7/SHA256SUMS.txt)；[本次 Mac 校验清单](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.11-macos-signed.1/SHA256SUMS.txt)。请按各平台实际下载版本核对。
- Windows 许可仍见其原 Release；本次 Mac 许可为对应 Release 的 `THIRD_PARTY_LICENSES.txt` 与 `THIRD_PARTY_NOTICES.md`，也随应用提供。

本仓库用于公开分发安装包和说明，应用源码由独立私有仓库维护。
