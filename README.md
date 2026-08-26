# VFlow AI — 本地多角色 AI 短视频一键成片工具

<p align="center">
  <img src="https://img.shields.io/badge/平台支持-Windows%20%7C%20Mac%20%7C%20Linux-blue?style=flat-square" alt="Platform">
  <img src="https://img.shields.io/badge/硬件加速-N卡CUDA%20%7C%20通用Vulkan%20%7C%20苹果Metal-orange?style=flat-square" alt="Hardware Acceleration">
  <img src="https://img.shields.io/badge/免环境配置-解压即用-success?style=flat-square" alt="Out of Box">
</p>

---

## 💡 这是什么？

**VFlow AI 是一款安装在你电脑本地的“全自动 AI 短视频制作工具”。**

只要输入一段故事、主题或文案，它就能全自动帮你：
1. **自动分镜头写剧本**
2. **自动给不同角色匹配专属声音配音**（支持声音克隆）
3. **自动用 AI 画出每个镜头的画面**
4. **自动对齐音频、压制字幕、剪辑合成完整高清短视频**

---

## 🌟 为什么选择 VFlow AI？（我们的核心优点）

- **零云端算力账单**：配音、画图和剪辑全靠你自己的电脑显卡跑，**没有按分钟计费的套路，想生成多少条视频就生成多少条**。
- **素材私密安全**：剧本、素材和生成的视频全部保存在自己电脑硬盘上，不上传云端，隐私不泄露。
- **免配置，解压双击就能用**：绿色免安装设计！不需要你折腾复杂的 Python 代码、不用装配置环境，下载解压直接运行。
- **主流显卡全支持**：不管你是英伟达 N 卡、AMD A 卡、Intel 显卡还是苹果 Mac，都能自动开启显卡加速。

> 📌 **新手小提示（关于大模型）**：
> 绘图、声音合成和视频剪辑全部在本地电脑完成；剧本大模型目前在设置中填入 API Key 即可使用（支持 DeepSeek、OpenAI 等，费用极低且自由）。

---

## 📥 软件下载 (Download)

前往页面右侧的 [**Releases 发布页面**](https://github.com/vtswcbyy/vflow-release/releases) 下载适合你电脑系统的安装包：

| 电脑系统 | 适合机型 | 加速类型 | 下载文件名 |
| :--- | :--- | :--- | :--- |
| **Windows 电脑** | 常见台式机 / 笔记本 (64位) | 支持 N卡 CUDA 加速 + 通用显卡加速 | `vflow-v*-windows-x86_64.zip` |
| **苹果 Mac 电脑** | 搭载 M1 / M2 / M3 / M4 芯片的 Mac | 原生 Apple Metal 芯片加速 | `vflow-v*-macos-arm64.tar.gz` |
| **Linux 电脑** | Ubuntu / Debian 等主流 64位系统 | CUDA + Vulkan 硬件加速 | `vflow-v*-linux-x86_64.tar.gz` |

> 💡 **下载小提示**：国内访问 GitHub 如遇下载较慢，可配合使用下载工具或网络加速。后续版本将同步上线 Hugging Face 与 魔搭 (ModelScope) 高速国内下载镜像。

---

## 🖥️ 我的电脑能跑吗？（硬件显存建议）

不用看复杂的参数，对照你的显卡显存对号入座即可：

| 硬件类型 | 显存 / 内存要求 | 运行效果 |
| :--- | :--- | :--- |
| **英伟达独立显卡 (N 卡)** | **建议 6GB 显存及以上**<br>*(最低 4GB 也能跑)* | 速度最快，AI 生图与声音合成秒级出结果 |
| **AMD 显卡 / Intel 显卡** | **建议 8GB 显存及以上** | 支持 Vulkan 通用加速，稳定运行 |
| **苹果 Mac 电脑** | **建议 16GB 统一内存及以上**<br>*(最低 8GB 也能跑)* | M 系列芯片原生优化，发热低运行流畅 |

*电脑内存建议 16GB 或以上，体验更佳。*

---

## 🚀 3步极速上手指南

1. **下载解压**：
   - 下载压缩包后，解压到任意文件夹（**建议解压路径不要带中文或空格**，例如解压到 `D:\vflow`）。
2. **双击启动**：
   - **Windows**：双击文件夹里的 `vflow.exe` 或 `launcher.exe`。
   - **Mac / Linux**：终端执行 `chmod +x ./vflow && ./vflow` 启动。
3. **开始制作**：
   - 启动后会自动在浏览器打开操作界面，在设置里填入你的大模型 API Key（如 DeepSeek），即可开始一键做视频！

---

## ❓ 常见问题 (FAQ)

<details>
<summary><b>Q1: 启动时提示显卡报错或无法开启加速？</b></summary>
请确保电脑具备独立显卡（或较新的 AMD/Intel 核显、苹果 M 芯片）。若是英伟达 N 卡，请使用 GeForce Experience 或官网驱动安装程序将显卡驱动更新到较新版本（推荐 550 以上）。
</details>

<details>
<summary><b>Q2: API Key 填在软件里安全吗？</b></summary>
非常安全。API Key 仅保存在你本地电脑的配置文件中，软件绝不会把你的 Key 上传给任何第三方。
</details>

<details>
<summary><b>Q3: 苹果 Mac 打开提示“无法验证开发者”？</b></summary>
进入 Mac 的「系统设置」 -> 「隐私与安全性」 -> 页面下方会显示被拦截的软件，点击「仍要打开」即可正常使用。
</details>

<details>
<summary><b>Q4: 需要自己安装 Python 或 Node.js 吗？</b></summary>
完全不需要！所有核心模块已经全部编译为独立的原生程序，下载解压就能直接用。
</details>

---

## 📢 交流与反馈

- **问题反馈**：如果在使用过程中遇到任何 Bug 或建议，欢迎在 GitHub 页面提交 [Issues](https://github.com/vtswcbyy/vflow-release/issues)。
