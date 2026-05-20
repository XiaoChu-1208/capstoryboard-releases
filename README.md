<p align="center">
  <img src="banner.svg" alt="CapStoryBoard CSP 分镜稿一键同步剪映" width="640" />
</p>

<p align="center">
  <video src="https://cdn.jsdelivr.net/gh/XiaoChu-1208/capstoryboard-releases@main/csb1.mp4" controls muted playsinline width="640"></video>
</p>

<p align="center">
  <video src="https://cdn.jsdelivr.net/gh/XiaoChu-1208/capstoryboard-releases@main/csb2.mp4" controls muted playsinline width="640"></video>
</p>

<h1 align="center">CapStoryBoard</h1>

<p align="center">
  <b>CSP 分镜稿一键切片同步到剪映工程的桌面工具 · Windows 原生应用</b>
</p>

<p align="center">
  在 Clip Studio Paint (CSP) 中绘制完整分镜稿 → 保存即自动按格切分为单镜 PNG →
  自动按 OCR 识别的镜号排序 → 复制到当前剪映工程素材库 → 按序铺入时间线。
  把动画 / 短视频 / 广告 / 漫画动态分镜从"画完手工导出 + 改名 + 拖入剪映"的两小时手活，压缩到 <b>保存即生效</b> 的零步骤。
</p>

<p align="center">
  <a href="https://github.com/XiaoChu-1208/capstoryboard-releases/releases/latest">
    <img alt="latest release" src="https://img.shields.io/github/v/release/XiaoChu-1208/capstoryboard-releases?label=Windows%20%E5%AE%89%E8%A3%85%E5%8C%85&color=e11d48">
  </a>
  <img alt="platform" src="https://img.shields.io/badge/Windows-10%20%7C%2011-0078d4">
  <img alt="offline" src="https://img.shields.io/badge/%E6%BF%80%E6%B4%BB%E5%90%8E-100%25%20%E7%A6%BB%E7%BA%BF-10b981">
  <img alt="license" src="https://img.shields.io/badge/%E6%8E%88%E6%9D%83-%E4%B9%B0%E6%96%AD%E5%88%B6-475569">
</p>

<p align="center">
  <a href="https://github.com/XiaoChu-1208/capstoryboard-releases/releases/latest"><b>下载最新版安装包</b></a> ·
  <a href="mailto:chizhu1208@163.com"><b>邮件联系作者购买兑换码</b></a> ·
  <a href="#常见问题"><b>常见问题</b></a> ·
  <a href="#技术架构与隐私">技术架构</a>
</p>

---

## 目录

- [适用人群与典型场景](#适用人群与典型场景)
- [核心功能](#核心功能)
- [工作流详解](#工作流详解)
- [系统要求](#系统要求)
- [下载与安装](#下载与安装)
- [购买流程](#购买流程)
- [兑换码与设备绑定](#兑换码与设备绑定)
- [自动更新机制](#自动更新机制)
- [常见问题](#常见问题)
- [技术架构与隐私](#技术架构与隐私)
- [作者与联系方式](#作者与联系方式)
- [版权与授权](#版权与授权)

---

## 适用人群与典型场景

CapStoryBoard 主要面向**自己用 CSP 画分镜、用剪映后期的内容创作者**，把"绘画 - 剪辑"两条工作流的中间衔接彻底自动化。

| 场景 | 传统流程 | CapStoryBoard 流程 |
|---|---|---|
| 动画短片预览（动态分镜） | 在 CSP 画完整张分镜稿 → 按格手工导出 50+ 张 PNG → 一张张改名（C001、C002 …） → 拖到剪映按顺序排好 → 调时长。**总耗时 1-2 小时** | 在 CSP 画完按 Ctrl+S → CapStoryBoard 后台**秒级**完成切片 + OCR 命名 + 推送到剪映时间线。**总耗时 0 步骤** |
| 短视频/Vlog 故事板 | 画完手工切图 → 用文件夹组织镜号 → 用 Excel/腾讯文档维护镜头表 | 切片 + 命名 + 镜头表同步一键完成 |
| 广告/MV 分镜评审 | 用 PS/PDF 拼一份故事板发给客户 | 直接导出可发的横/竖屏 PDF 故事板 + 资产 ZIP |
| 漫画动态分镜（动漫化预演） | 同上 | 同上 + 自动按页对齐 16:9/9:16 安全框 |

如果你符合下面任何一条，CapStoryBoard 就是为你做的：

- 经常在 **Clip Studio Paint** 里画分镜稿，然后拿到 **剪映** 里做动态预览
- 每次画完都要花十几分钟切图、改名、拖入素材库
- 希望分镜稿改一笔，剪映工程**自动跟着变**
- 担心把分镜稿和创意上传到云端（云盘/在线分镜工具）

---

## 核心功能

### 1. CSP 文件实时监听 + 自动切片

CapStoryBoard 会监听你指定的 CSP 工程目录。当你按 `Ctrl+S` 保存 `.clip` 文件时：

- 自动读取最新的画布
- 按你预设的分镜格网（常用 2×4 / 3×3 / 4×6 等）切分为单格 PNG
- 切片分辨率默认输出每镜 **1920×1080**（可在偏好设置改 2K / 4K / 自定义）
- 输出格式：透明背景 PNG，支持线稿 / 上色 / 合成三种图层组合

### 2. OCR 镜号识别

如果你在每格分镜稿的左上角写了镜号（`C01`、`S01C001`、`Cut-01` 等格式）：

- 内置 **rapidocr-onnxruntime** 离线 OCR 引擎识别每格的镜号文本
- 按识别到的镜号**自动排序**，不再依赖你画的顺序
- 支持的镜号命名约定：`S{场次}C{镜号}` / `C{镜号}` / `Scene{N}-{N}` 等
- 识别失败的格会用文件名后缀 `_?` 标记，方便你回去补镜号

### 3. 剪映工程直接对接

支持剪映**桌面专业版**（JianyingPro / CapCut Pro）的工程文件结构：

- 自动识别当前打开的剪映项目（解析 `~/AppData/Local/JianyingPro/User Data/Projects/...`）
- 切片完成的 PNG 自动复制到该工程的素材库目录
- 按镜号顺序**自动铺到主轨道**，每镜默认 2 秒（可在剪映里手动调时长）
- 支持横屏 16:9 / 竖屏 9:16 / 方形 1:1 / 自定义比例

### 4. 一键导出可交付的故事板

完成后一键导出：

- **PDF 故事板**：横/竖屏可选，每页 4-12 镜可调，自动标注镜号 + 备注
- **ZIP 资产包**：所有切片 PNG + 镜头表 CSV + 元信息 JSON，发给制片 / 后期 / 导演评审

### 5. 完全离线运行

激活后**所有功能本地完成**：CSP 解析、OCR 识别、PNG 切片、PDF 打包、剪映对接全部在本机进行。
你的草稿、剧本、剪辑工程**永远不会**上传到任何服务器。

---

## 工作流详解

### 第一次启动

1. 启动 App，选择你的剪映工程目录（默认会自动检测 `~/AppData/Local/JianyingPro/User Data/Projects`）
2. 选择你的 CSP 分镜工作目录（任意指定）
3. 配置一次分镜格网：行数 × 列数，单镜输出分辨率，镜号命名约定
4. 点"开始监控"，App 缩到系统托盘

### 日常使用

1. 在 CSP 里画分镜，每格左上角写镜号（推荐 `C01`、`C02` …）
2. 按 `Ctrl+S` 保存
3. CapStoryBoard 托盘图标短暂闪动（约 2-5 秒处理）
4. 切回剪映 → **新的分镜镜头已经按顺序铺在主轨道上**

如果你改了某一格画面：再次保存 → 对应那一镜的 PNG **自动覆盖更新**，剪映里那一镜跟着变。

### 评审输出

1. 在 App 主界面点"分镜编排"切回横/竖屏视图
2. 调整每镜时长 / 备注 / 转场
3. 点"导出 PDF"或"打包 ZIP"

---

## 系统要求

| 项目 | 要求 |
|---|---|
| 操作系统 | Windows 10（1903 +）/ Windows 11，64-bit |
| 内存 | 4 GB 及以上（推荐 8 GB+） |
| 磁盘 | 安装包占 100 MB，运行时缓存约 200-500 MB |
| WebView2 运行时 | Win11 内置；Win10 通过 Microsoft Edge 自动安装；缺失时安装向导会提示 |
| 必需软件 | **Clip Studio Paint**（v1.10+）+ **剪映专业版 / CapCut Pro**（4.0+） |
| 网络 | 仅**首次激活**需要约 2 秒，激活后无需联网 |

> macOS 版正在规划中，目前**仅支持 Windows**。

---

## 下载与安装

到 [Releases 页](https://github.com/XiaoChu-1208/capstoryboard-releases/releases/latest) 下载最新 `CapStoryBoardSetup-X.Y.Z.exe`。

### 安装步骤

1. **双击 `CapStoryBoardSetup-0.1.0.exe`**
2. 安装向导是 5 步流程：
   - **欢迎页**：点击"开始部署"
   - **输入授权码**：粘贴作者发给你的 `CSB-XXXX-XXXX-XXXX` 兑换码
   - **选择安装目录**：默认 `%LocalAppData%\Programs\CapStoryBoard`，**无需管理员权限**
   - **释放部署**：实时显示拷贝进度 + 安装日志，约 5-10 秒
   - **完成**：可选"立即启动 CapStoryBoard"
3. 安装完成后桌面会有快捷方式；开始菜单的程序列表里也能找到

### 卸载

通过 Windows "应用与功能" → "CapStoryBoard" → 卸载。
卸载**不会**删除你的激活信息（`%USERPROFILE%\.capstoryboard\license.json`），重装后无需重新激活。

---

## 购买流程

CapStoryBoard 是**买断制付费软件**（一次性付费，永久使用，无订阅）。

### 完整购买步骤

1. **发送购买意向邮件**到作者邮箱 `chizhu1208@163.com`
   - 邮件主题建议写：`CapStoryBoard 购买咨询`
   - 邮件内容请说明：你的用途（个人 / 工作室）、是否需要发票、希望的支付方式（微信 / 支付宝 / 银行转账）
2. **作者回复价格 + 付款信息**（通常当天回复）
3. **完成付款** → 把付款凭证截图发回邮件
4. **作者当场签发 18 位兑换码**，邮件回复给你，形如：
   ```
   CSB-A3F1-X8K2-9VBM
   ```
5. **下载安装包** → 在安装向导第 2 步「输入授权码」粘贴上面的兑换码
6. **完成安装** → App 首次启动会通过 HTTPS 联网完成绑定（约 2 秒），**绑定到你这台电脑**
7. 之后所有功能本地可用，**完全离线**

### 试用与退款

- **暂未提供试用版本**。如需了解功能细节，可以邮件向作者要演示视频
- **退款**请在购买后 **7 天内**邮件申请，未激活的兑换码全额退款；已激活的按使用情况协商

---

## 兑换码与设备绑定

CapStoryBoard 采用**设备指纹绑定的离线激活机制**：每张兑换码会锁死在第一次激活的电脑上，**不能转给朋友、不能在多台机器同时用**。

### 兑换码格式说明

- 18 个字符（含 2 个连字符）
- 形如 `CSB-XXXX-XXXX-XXXX`
- 字符集 32 字符：`A-Z 2-9`，**不含**易混字符 `I` / `O` / `0` / `1`
- 每张兑换码**全网唯一**，由 Upstash Redis 维护一致性

### 设备绑定原理

激活时 App 会计算本机的设备指纹（MAC 地址 + 主机名 + 平台标识 SHA-256 哈希前 4 字节 → 8 位十六进制）发到作者的服务器一次。
服务器用 Ed25519 私钥签发一张**只有这个设备指纹能用**的离线许可证（`license.json`），写入本机后**永久离线运行**。

### 关于密钥的常见疑问

| 问 | 答 |
|---|---|
| 兑换码能在多台电脑上用吗？ | **不能**。每张兑换码会锁定到首次激活的设备指纹。 |
| 我换电脑了怎么办？ | 联系作者邮件说明，作废原码并补发一张新码。这是正常售后流程。 |
| 我重装了 Windows？ | 通常 MAC 地址不变 → 指纹不变 → 直接用原 `license.json` 即可。如果激活报错，按"换电脑"流程申请新码。 |
| 我换了网卡 / 装了独立网卡？ | MAC 变了 → 指纹变了 → 需要联系作者重发新码。 |
| 卸载并重装会丢激活吗？ | **不会**。`license.json` 在 `%USERPROFILE%\.capstoryboard\`，不在程序目录里，卸载不动它。 |
| 哪里能看激活信息？ | 启动 App → 偏好设置（齿轮图标） → 授权信息 |
| 我能否反编译 / 二次分发？ | **不可以**，详见 [版权与授权](#版权与授权)。 |

---

## 自动更新机制

App 启动时会自动检查新版本：

- 从本仓库 `main` 分支拉取一个 5 KB 的 [`manifest.json`](https://github.com/XiaoChu-1208/capstoryboard-releases/blob/main/manifest.json)
- 比对 `latest` 字段与本机版本号
- 有新版可用时，**欢迎页右上角会出现红色向上箭头角标**
- 点击角标会弹出版本说明 + "前往下载"按钮，跳转到本仓库 Releases 页

### 隐私保证

- 检查更新**只发一次 HTTPS GET 请求**到 GitHub Raw CDN，**不携带任何账号 / 用户 / 机器信息**
- 不上报 App 版本 / 操作系统 / IP 等任何遥测数据
- 可以在偏好设置里关闭自动检查

### 升级方式

下载新版安装包 → 覆盖安装 → 完成。
**无需重新激活**，原 `license.json` 自动保留。

---

## 常见问题

### 安装阶段

#### Q: 安装向导报"兑换码格式不正确"

检查清单：
- 兑换码完整 18 个字符，含 `CSB-` 前缀
- 包含 2 个短横线，应为 `CSB-XXXX-XXXX-XXXX` 形式
- 没有多余空格 / 换行（从作者邮件**复制时 Ctrl+A 全选邮件正文容易带换行**，建议双击只选兑换码本身）
- **不含**字母 `I`、`O` 和数字 `0`、`1`（设计上规避混淆字符）

#### Q: 安装向导启动后白屏或闪退

可能原因：缺少 WebView2 运行时。

解决方案：
1. 打开 Microsoft Edge → "关于" → 让 Edge 自动更新到最新（会顺带装 WebView2）
2. 或手动安装：https://developer.microsoft.com/microsoft-edge/webview2/
3. 装完后重新运行安装包

#### Q: 安装到 `C:\Program Files\` 失败

CapStoryBoard 默认装到 `%LocalAppData%\Programs\CapStoryBoard`，**不需要管理员权限**。
如果你手动改到 `Program Files`，需要在弹出的 UAC 提示中点"是"授权。
**不推荐改默认路径**，除非你有运维理由。

### 激活阶段

#### Q: App 首次启动报"激活失败：兑换码不存在"

可能：
- 兑换码输入有误（多 / 少字符 / 大小写）
- 兑换码已被作废（请邮件联系作者核对）
- 你的网络无法访问 `storycut.work`（HTTPS 端点）

排查：
1. 暂时关闭 VPN / 代理（部分代理会拦截）
2. 在浏览器打开 https://www.storycut.work 看是否能正常访问
3. 不行的话联系作者，提供你的设备指纹（启动 App 时报错提示里会显示）

#### Q: App 报"此密钥已绑定其他设备"

这张兑换码已经在另一台电脑激活过了。按 [换电脑流程](#兑换码与设备绑定) 联系作者申请新码。

#### Q: App 报"无法连接激活服务器"

可能：
- 网络问题（防火墙 / 代理 / 断网）
- 服务器临时维护（极少发生）
- 请重试 / 换网络环境 / 联系作者

### 使用阶段

#### Q: 切片输出的镜号顺序不对

OCR 偶尔会把手写镜号识别错（例如把 `C7` 读成 `C1`）。解决方法：
- 镜号写工整一些，建议用直线笔刷而非毛笔
- 镜号位置固定在每格左上角（不要写到画面正中或角落）
- 镜号字号占整格高度的 5-10%（太小识别不到，太大干扰画面）
- 在 App 偏好设置里可以**手动覆盖**自动识别结果

#### Q: 剪映里没看到新加的镜头

排查：
1. 检查 App 主界面是否显示"监控中"状态
2. 检查剪映工程是否正确识别（主界面顶部应该显示当前剪映工程名）
3. 在剪映里手动刷新素材库（右键 → 刷新）

#### Q: PDF 故事板导出后排版异常

- 检查 CSP 分镜稿的格网比例是否与 App 偏好设置一致
- 尝试切换 PDF 模板（App → 分镜编排 → 模板选择）

### 法务与商务

#### Q: 可以申请退款吗？

可以。购买 7 天内未激活的兑换码可**全额退款**；已激活的按使用情况协商。
退款申请请邮件 `chizhu1208@163.com`，主题 "CapStoryBoard 退款申请"。

#### Q: 可以开发票吗？

可以。请在购买时邮件说明，备注公司名 / 税号 / 收件邮箱。

#### Q: 团队 / 工作室批量购买有折扣吗？

5 张及以上批量购买有折扣，详询作者邮箱。

---

## 技术架构与隐私

### 软件构成

CapStoryBoard 由两部分构成：

1. **桌面应用**（本仓库分发）—— Windows 原生 .exe，PyInstaller 单文件打包
   - GUI 层：pywebview + Microsoft WebView2 渲染（基于 Edge Chromium）
   - 业务层：Python 3.12，主要依赖 PIL（图像）、psd-tools（CSP 解析）、watchdog（文件监听）、rapidocr-onnxruntime（OCR）、nacl（Ed25519 验签）
   - 切片 / 渲染走纯本地 CPU，不调用任何云端 OCR / 图像处理 API
2. **激活服务**（作者私有部署）—— Vercel + Upstash Redis
   - 作用：根据兑换码查询订单记录，签发**绑定到设备指纹的**离线许可证
   - 仅在**首次激活那一次**通讯，之后客户端与服务端**完全没有通讯**

### 数据流

激活时（一次性）：
```
客户端                          作者服务器
  │                                │
  │  POST /api/license/activate    │
  │  { code, device_id }           │
  │ ─────────────────────────────> │
  │                                │  查 Upstash 验证 code
  │                                │  Ed25519 签发 license
  │                                │
  │  { license: "CSB-... (long)" } │
  │ <───────────────────────────── │
  │                                │
  │  本地验签 + 写 license.json    │
  │  (从此完全离线)                │
```

激活后（永久）：
- 客户端**不再向作者服务器发送任何请求**
- 除非用户主动检查更新（GET 一个 5KB 的 manifest.json，不带任何用户信息）

### 隐私承诺

CapStoryBoard 不收集、不上报、不传输以下数据：

- 你的 CSP 草稿内容（`.clip` 文件）
- 你的 PSD 文件 / 切片 PNG / 任何中间产物
- 你的剪映工程文件 / 视频素材
- 任何使用统计 / 错误堆栈 / 崩溃日志
- 你的网络 IP、操作系统版本、硬件信息
- 任何可识别你身份的元数据

唯一会离开本机的数据：
- **激活时**：你的兑换码（你已经知道）+ 8 位十六进制设备指纹（MAC + 主机名 + 平台的 SHA-256 哈希前 4 字节，**不可逆，不含个人信息**）
- **检查更新时**：拉取一个公开的 5KB JSON，**不携带任何 header / body 个人信息**

### 反盗版

- 兑换码经 Ed25519 签名绑定到设备指纹，**反编译客户端也无法生成新码**（私钥从不离开作者本机）
- 验签发生在客户端本地，**断网也无法绕过**（签名校验是数学保证，不是服务端口令）
- 你的同事 / 朋友拿你的 `license.json` 也用不了，因为他们的设备指纹对不上

### 开源情况

- 本仓库（capstoryboard-releases）**公开**：包含 README、banner、manifest、release 安装包
- 源代码仓库（capstoryboard）**不公开**：商业软件，源码保留作者所有权
- Ed25519 验签代码可在反编译产物中查阅（出于透明度，验签逻辑就是公开标准）

---

## 作者与联系方式

CapStoryBoard 由独立开发者 **小刍 (XiaoChu-1208)** 开发并维护。

- **作者邮箱**: chizhu1208@163.com（购买 / 退款 / 售后 / 反馈，**通常 24 小时内回复**）
- **问题反馈**: 本仓库的 [Issues 页](https://github.com/XiaoChu-1208/capstoryboard-releases/issues)（推荐附 App 版本号 + 错误截图 + 操作步骤）
- **作者主页**: https://github.com/XiaoChu-1208

### 在做但还没发的功能

- macOS 版本（计划中）
- Toon Boom Harmony / TVPaint / Procreate 工程对接（看反馈）
- 团队协作 / 工作室共享分镜库（看反馈）
- 多剪映工程同时监控（v0.2 计划）

如果你对某个功能有强烈需求，欢迎发邮件投票。

---

## 版权与授权

CapStoryBoard 是商业付费软件，著作权归作者所有。

**允许的行为**：
- 个人 / 团队购买后自用
- 评测 / 推荐 / 引用（请注明出处 + 链接）
- 学习目的反编译查看激活流程实现

**禁止的行为**：
- 未授权分发安装包 / 兑换码
- 移除 / 篡改激活逻辑后二次分发
- 把 CapStoryBoard 的功能集成进其他商业软件
- 利用本软件搭建二次盈利的在线服务

商务合作 / OEM 授权请直接邮件联系作者。

---

<p align="center">
  <sub>Copyright © 2026 XiaoChu-1208. All rights reserved.</sub><br>
  <sub>关键词：剪映分镜 · Clip Studio Paint 分镜 · CSP 切片 · 故事板软件 · 镜号 OCR · 离线分镜工具 · Storyboard for JianyingPro · CapCut storyboard automation · Windows 桌面分镜软件</sub>
</p>
