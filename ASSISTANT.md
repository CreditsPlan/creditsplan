# CreditsPlan 助手

CreditsPlan 的 Windows 桌面客户端：查看 Codex、Claude Code 的本机用量统计，并使用 CreditsPlan 账号访问在线顾问等功能。

## 下载

**[下载 Windows x64 安装包](https://github.com/CreditsPlan/creditsplan/releases/latest/download/CreditsPlan-Assistant-windows-x64-setup.exe)**

[查看全部版本和更新说明](https://github.com/CreditsPlan/creditsplan/releases)

下载 `.exe` 安装包即可安装。GitHub 自动提供的 `Source code` 压缩包只包含本下载仓库的说明文件，不是安装程序。

当前安装包未做 Windows 代码签名，Windows 可能显示“未知发布者”或 SmartScreen 提示，部分设备的安全策略可能阻止安装。每个发布版本都附有 SHA-256 校验文件，供核对下载文件。

首次安装可能需要联网安装 Microsoft WebView2。官网登录、顾问和云同步功能需要联网。

当前采用手动更新：新版本发布后，从这里下载新的安装包。

## 本机统计与隐私

助手默认读取当前 Windows 账号下受支持的 Codex、Claude Code 会话日志，提取用量统计并保存在本机；原始日志不会被修改。

云同步默认关闭。登录并主动开启同步后，助手上传用于账号用量分析的统计数据，不上传原始日志或对话正文。可在助手中暂停统计、管理同步及清理数据。

用量和成本分析供参考，不等同于服务商账单。

## 帮助

- 官网：[creditsplan.ai](https://creditsplan.ai)
- 问题反馈：[官网反馈入口](https://creditsplan.ai/feedback/)
- 第三方声明见 `THIRD_PARTY_NOTICES.md`，依赖许可见每个发布版本附带的 `THIRD_PARTY_LICENSES.txt`。

本仓库用于公开分发安装包和说明，应用源码由独立私有仓库维护。
