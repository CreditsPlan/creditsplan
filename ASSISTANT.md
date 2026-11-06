# CreditsPlan 助手

CreditsPlan 的 Windows / Mac 桌面客户端：查看受支持工具（包括 Codex、Claude Code）的本机用量统计，并使用 CreditsPlan 账号访问在线智能选型等功能。

## 服务与账户

当前公开安装包为连接 **[creditsplan.ai](https://creditsplan.ai/)** 的国际版，使用国际服务的账户、会话和 Credits。中文界面不会改变其连接的服务。

[国内智能选型](https://ai.creditsplan.cn/) 是独立服务，账户、会话和 Credits 不与国际服务自动互通。国内中文桌面版暂未发布，当前请使用国内网页版。

## 下载

**[官网下载中心](https://creditsplan.ai/download/)** · 以下版本已对照公开 GitHub Releases 核对（2026-11-06），按平台分别选择。

| 平台 | 版本 | 下载 | 文件大小 | 发布日期（UTC） |
| --- | --- | --- | --- | --- |
| Windows x64 | 0.1.17 | [EXE 安装包](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.17/CreditsPlan-Assistant-windows-x64-setup.exe) | 10,708,788 字节 | 2026-10-30 |
| Mac · Apple Silicon（M 系列） | 0.1.18 | [arm64 DMG](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.18/CreditsPlan-Assistant-macos-arm64.dmg) | 15,168,382 字节 | 2026-11-03 |

[查看全部版本和更新说明](https://github.com/CreditsPlan/creditsplan/releases)

Windows 下载 `.exe` 安装包；Mac M 系列芯片下载 Apple Silicon 的 `.dmg`。GitHub 自动提供的 `Source code` 压缩包只包含本公开仓库的说明文件，不是安装程序，也不包含应用业务源码。

## Mac 安装与更新

1. 在苹果菜单“关于本机”查看芯片：仅支持 Apple Silicon（M 系列），**不支持 Intel Mac**，要求 macOS 11.0 或更高版本。
2. 下载 DMG，核对 [Mac SHA-256 校验清单](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.18/SHA256SUMS.txt)，将“CreditsPlan 助手”拖入 Applications（应用程序），再从应用程序打开。
3. App 与 DMG 已使用 Developer ID 正式签名并通过 Apple 公证。首次启动可能出现正常的“从互联网下载的应用”确认，核对来源后点击“打开”。若签名验证失败，请停止安装并反馈错误，不要关闭系统安全保护。

**旧版 Mac 客户端需手动安装 0.1.18 一次，以启用后续应用内更新。** 之后可在应用内检查并确认更新，等待完整更新包下载、签名校验和安装，再按提示重启。

安装方法和本次发布验收记录见 [0.1.18 发行说明](https://github.com/CreditsPlan/creditsplan/releases/tag/assistant-v0.1.18)；平台构建信息见 [Mac 发布清单](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.18/release-manifest-macos-arm64.json)。

## Windows 安装与更新

Windows 安装包未做代码签名，可能显示“未知发布者”或 SmartScreen 提示，部分设备的安全策略可能阻止安装。下载后请核对 [Windows SHA-256 校验清单](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.17/SHA256SUMS.txt)。

首次安装可能需要联网安装 Microsoft WebView2。登录、在线智能选型和云同步功能需要联网。

Windows 当前采用手动更新：新版本发布后，从公开发行页下载新的安装包。版本与构建信息见 [0.1.17 发行说明](https://github.com/CreditsPlan/creditsplan/releases/tag/assistant-v0.1.17) 和 [Windows 发布清单](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.17/release-manifest.json)。

## 启动器支持范围

Windows 当前自动发现 Cursor，其他受支持桌面工具需要手动添加。Mac 启动器尚未实现，应用会保留“不支持”的限制。

## 本机统计与隐私

本机统计无需登录。助手读取当前系统账号下受支持工具的本机用量记录，提取统计数据并保存在本机；不会修改原始会话日志。Codex 与 Claude Code 的标准会话日志目录包括 `~/.codex/sessions`、`~/.codex/archived_sessions` 和 `~/.claude/projects`。`~` 对应当前系统用户的主目录；其他工具的支持范围以所安装版本中的说明为准。

云同步默认关闭。登录并主动开启同步后，助手上传用于账号用量分析的统计数据，不通过用量同步上传原始日志或对话正文。你主动发送给在线智能选型的消息会交由在线服务处理。可在助手中暂停统计、管理同步及清理数据。

用量和成本分析供参考，不等同于服务商账单。反馈问题时请提供系统、助手版本和症状，不要发送密钥、原始对话或完整会话日志。

## 帮助与许可

- 国际服务：[creditsplan.ai](https://creditsplan.ai/)
- 国内网页版：[ai.creditsplan.cn](https://ai.creditsplan.cn/)
- 国际服务反馈：[官网反馈入口](https://creditsplan.ai/feedback/)
- Windows：[第三方许可证](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.17/THIRD_PARTY_LICENSES.txt) · [第三方声明](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.17/THIRD_PARTY_NOTICES.md)
- Mac：[第三方许可证](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.18/THIRD_PARTY_LICENSES.txt) · [第三方声明](https://github.com/CreditsPlan/creditsplan/releases/download/assistant-v0.1.18/THIRD_PARTY_NOTICES.md)

本仓库用于公开分发安装包和说明，应用源码由独立私有仓库维护。许可与第三方声明请按实际下载的平台和版本核对。
