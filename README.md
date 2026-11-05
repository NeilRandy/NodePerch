<h2 align="center">
  <a href="https://github.com/NeilRandy/NodePerch/releases/download/v0.4.0/NodePerch-0.4.0-win-x64.zip">⬇ 下载 Windows 版 · v0.4.0</a>
</h2>
<p align="center">
  公开预览版 · Windows x64<br>
  <a href="#安装与连接">安装与连接</a> ·
  <a href="使用说明.md">使用说明</a> ·
  <a href="https://github.com/NeilRandy/NodePerch/releases">全部版本</a>
</p>

![NodePerch：五秒采样、十分钟曲线、多机总览](images/hero.png)

![历史曲线：每台启用主机独立采样，切换时直接读取十分钟缓存](images/history.png)

![多机总览：查看各主机的 CPU、GPU、可用内存和显存，点击进入详情](images/overview.png)

![添加主机：选择已有 SSH 配置或手动填写连接信息](images/connect.png)

<sub>以上为真实界面与演示数据。曲线保存在本次运行的内存中，退出后清空。</sub>

## 安装与连接

1. **下载并解压** [Windows 运行包](https://github.com/NeilRandy/NodePerch/releases/download/v0.4.0/NodePerch-0.4.0-win-x64.zip)，双击 `NodePerch.exe`。请完整解压，不要只复制 EXE。
2. **添加主机**：选择 SSH 别名，或手动填写地址、用户名、端口和私钥路径。
3. **检查登录**：首次连接可点“检查 SSH 登录”，在终端核实主机指纹并检查登录，完成后输入 `exit`。
4. **开始查看**：点击“添加并连接”，收到数据后即可使用。后台采集需要密钥或 SSH agent 免交互登录；仅能手动输入密码的连接尚不能用于持续采集。

> 请下载名称为 `NodePerch-0.4.0-win-x64.zip` 的运行包。GitHub 的 Code → Download ZIP 和自动生成的 Source code 仅包含介绍资料，不能运行程序。需要校验下载文件时，可使用 [SHA-256 校验文件](https://github.com/NeilRandy/NodePerch/releases/download/v0.4.0/NodePerch-0.4.0-win-x64.zip.sha256)。

### 运行要求

| 位置 | 要求 |
| --- | --- |
| 本机 | 64 位 Windows、.NET Framework 4.8、OpenSSH 客户端 |
| Linux 主机 | SSH 服务、登录权限、`/usr/bin/python3` |
| Windows 主机 | SSH 服务、登录权限、PowerShell 5.1 |
| NVIDIA GPU 指标 | 远端可执行 `nvidia-smi`；没有 NVIDIA 显卡仍可查看 CPU、内存等指标 |

本机无需安装 Python，远端无需安装常驻监控服务。程序不保存密码或私钥内容，也不修改 SSH 配置。

### 使用与更新

- 点“×”收起到托盘并继续采样；托盘菜单中的“退出”才会彻底关闭程序。更新前请先退出旧版。
- 主机、启用状态和主题保存在 `%LOCALAPPDATA%\SharedResourceDashboard\settings.json`，更新程序可沿用。
- 进程筛选、暂停主机、编辑连接等操作见[使用说明](使用说明.md)。

## 反馈

遇到问题或有功能建议，可以[提交 Issue](https://github.com/NeilRandy/NodePerch/issues)。请附软件版本、远端系统、操作步骤和错误文字；截图请遮盖不希望公开的主机信息，不要上传密码、私钥或个人 SSH 配置。

已发布功能见[版本记录](CHANGELOG.md)。

## 署名与许可

Copyright © 2026 **RandyNeil**。

NodePerch 采用**非商业许可**。个人学习、非商业教学与科研可免费使用；免费转发完整原版时须保留署名和许可。商业使用、商业集成、收费部署，以及向本人或所在课题组以外分发修改版，需要作者另行书面授权。

使用范围以发行包内的 [LICENSE.txt](LICENSE.txt) 为准。如需讨论授权，可先在仓库提出请求；公开留言本身不代表已获得授权。
