# Studio 0 — Modbus 调试工具（发行版）

<p align="center">
  <strong>专业级 Modbus 协议调试与仿真工具 · 免费发布版</strong><br/>
  <em>支持 Modbus RTU / TCP / ASCII | 主站 / 从站</em>
</p>

---

> 📦 **本仓库仅发布编译好的免费使用版本（Release 安装包），不提供源代码。**
> 如需使用，请直接下载下方 Release 中的 `Studio 0 Release 4.3.4.43.zip` 解压即用。

## ✨ 功能概览

### 📡 协议支持
| 协议类型 | 传输方式 | 支持模式 |
|---------|---------|---------|
| **Modbus RTU** | 串口 (COM) | 主站 / 从站 |
| **Modbus TCP** | 以太网 (TCP/IP) | 主站 / 从站 |
| **Modbus ASCII** | 串口 (COM) | 主站 / 从站 |

### 🛠 核心功能
- **数据采集监控** — 实时读写寄存器、线圈、离散输入，支持自定义刷新周期
- **指令下发** — 单点/批量写入寄存器和线圈，支持十六进制/十进制/浮点格式
- **从站仿真** — 模拟 Modbus 从设备，自定义数据映射表，用于上位机联调测试
- **多设备管理** — 同时连接多台设备，独立配置每台设备的通讯参数
- **数据日志** — 完整记录所有通讯报文（请求/响应），支持导出分析
- **图形组态** — 自定义数据可视化界面（仪表盘、曲线图、状态灯等）
- **脚本自动化** — 内置 Python 脚本引擎，支持定时任务和条件触发
- **报警系统** — 多级阈值报警，声音/弹窗/邮件通知

---

## 📥 下载与安装

1. 进入 [Releases](https://github.com/EveryIsZero/Studio-0/releases) 页面
2. 下载最新版本 `Studio 0 Release 4.3.4.43.zip`
3. 解压到任意目录（建议非中文路径）
4. 双击 `Studio 0.exe` 启动
5. 首次运行会自动生成配置目录

> ✅ **无需安装 Python 或任何运行环境，开箱即用。**

---

## 📦 发布包内容
解压 `Studio 0 Release 4.3.4.43.zip` 后目录结构如下：
```
Studio 0/
├── Studio 0.exe           # 主程序（双击启动，无需安装 Python）
├── _internal/             # Python 运行时（必须与 exe 同级，勿删除）
├── cfg/                   # 用户配置目录（运行时自动生成）
└── readme.txt             # 版本迭代记录
```
> ⚠️ 请保持 `Studio 0.exe` 与 `_internal/` 在同一目录下，否则无法启动。

---

## 🔧 使用说明

### 1. 新建连接
点击工具栏「新建连接」→ 选择协议类型 (RTU/TCP/ASCII) → 配置端口/IP 参数 → 点击「连接」

### 2. 配置数据点
在数据配置面板中添加需要监控的寄存器：
- 设置地址、数量、数据类型
- 配置读取周期和数据系数
- 可选设置字节序和解析规则

### 3. 开始监控
选中数据点 → 点击「启动采集」→ 实时查看数据变化

### 4. 数据写入
在数值列双击或右键 → 输入新值 → 确认下发

### 5. 从站仿真
切换到「从站模式」→ 配置本地数据映射 → 等待主站连接

---

## 📋 版本历史

当前版本: **4.3.4.43** (v4.3.4.43)

详细变更记录请参见 [Releases](https://github.com/EveryIsZero/Studio-0/releases) 页面。

---

## 📄 软件许可

本软件为 **免费软件（Freeware）**，供个人与商业用途免费使用，**不提供源代码**。
你可以自由下载、分发本安装包，但不得对其进行逆向工程、破解或用于非法用途。
版权所有 © EveryIsZero。

---

## 💬 反馈与交流

使用中遇到问题或有功能建议，欢迎在 [Issues](https://github.com/EveryIsZero/Studio-0/issues) 中反馈。

---

## ☕ 支持作者

如果这个工具对你有帮助，欢迎请作者喝杯咖啡 ☕ 你的支持是持续维护的动力！

<p align="center">
  <table>
    <tr>
      <td align="center">
        <strong>微信支付</strong><br/><br/>
        <img src="donate/wechat_qr.png" width="220"/><br/>
        <em>微信扫一扫</em>
      </td>
      <td width="40"></td>
      <td align="center">
        <strong>支付宝</strong><br/><br/>
        <img src="donate/alipay_qr.jpg" width="220"/><br/>
        <em>支付宝扫一扫</em>
      </td>
    </tr>
  </table>
</p>

---

<p align="center">
  <sub>Made with ❤️ by <a href="https://github.com/EveryIsZero">EveryIsZero</a></sub>
</p>
