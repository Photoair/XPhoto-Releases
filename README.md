# XPhoto

商业人像精修桌面工具（Windows 10 / 11 x64）。

> 本仓库**仅用于分发安装包**，源代码不在此公开。

---

## 下载 / Download

前往 **[Releases](https://github.com/Photoair/XPhoto-Releases/releases)** 页面下载最新版本。

### 最新版 v1.1.1

| 版本 | 说明 | 下载 |
|---|---|---|
| **安装版**（推荐） | 自动创建开始菜单/桌面快捷方式，可选安装目录 | [XPhoto Setup 1.1.1.exe](https://github.com/Photoair/XPhoto-Releases/releases/download/v1.1.1/XPhoto%20Setup%201.1.1.exe) |
| **便携版** | 免安装，双击即用，可放 U 盘 | [XPhoto-1.1.1-便携版.exe](https://github.com/Photoair/XPhoto-Releases/releases/download/v1.1.1/XPhoto-1.1.1-%E4%BE%BF%E6%90%BA%E7%89%88.exe) |

体积约 113 MB / 个。系统要求：Windows 10 / 11（x64）。

> **首次使用 AI 功能需要联网**下载模型（约 112 MB），之后可离线使用。

---

## v1.1.1 更新要点

- **修复「打开图片就崩溃」** —— 程序现在**自带 VC++ 运行库**，不再受系统运行库版本不一致的影响。那正是 AI 推理库（onnxruntime）崩溃的根因。
- **崩溃兜底与取证**：异常退出会记录日志与崩溃转储；检测到上次崩在 onnxruntime 时会**自动停用 AI 功能**，避免反复崩溃。
- **崩溃提示如实**：弹窗会写出检测到的运行库版本与修复办法，而不是一句"出错了"。
- **修复「更新检查」**：之前读错了文件名，导致收不到新版本提示。

<details>
<summary>English</summary>

**XPhoto** is a portrait retouching desktop app for Windows 10/11 (x64).

**v1.1.1 fixes "crash on opening an image":** the app now ships its own VC++ runtime, so it no longer depends on the system-wide runtime version — the actual root cause of crashes inside the AI inference library (onnxruntime). It also adds crash logging/dump forensics, automatic AI fallback after a native crash, and honest error dialogs.

Download from the **[Releases](https://github.com/Photoair/XPhoto-Releases/releases)** page. AI features download their models (~112 MB) on first use.

</details>
