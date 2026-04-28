# Install

Bilingual install guide for Bamdra Loom · 双语安装指南

> **For everyone — no developer experience needed.** Once installed, see the
> [quickstart in English](docs/en/01-quickstart.md) or [中文上手](docs/zh/01-quickstart.md)
> for what to do next.

---

## English

### macOS

1. Download the `.dmg` matching your chip:
   - Apple Silicon: `Bamdra Loom_<version>_aarch64.dmg`
   - Intel: `Bamdra Loom_<version>_x64.dmg`
2. Open the dmg and drag **Bamdra Loom** into Applications.
3. The first launch will say "unidentified developer". Right-click the app → **Open**, then confirm in the dialog. macOS remembers the choice.

#### If you see "damaged and can't be opened"

We do not have a paid Apple Developer account, so the app is ad-hoc signed instead of notarized. If the system flags it as damaged (usually after the file went through email/Slack/quarantine), clear the quarantine attribute once:

```bash
xattr -cr "/Applications/Bamdra Loom.app"
```

Then double-click again.

### Windows

1. Download `Bamdra Loom_<version>_x64-setup.exe`.
2. Run it. Windows SmartScreen may show a warning — click **More info** → **Run anyway**.
3. Follow the installer.

### Linux

#### deb (Debian / Ubuntu / derivatives)

```bash
sudo dpkg -i bamdra-loom_<version>_amd64.deb
sudo apt-get install -f
```

#### AppImage

```bash
chmod +x Bamdra\ Loom_<version>_amd64.AppImage
./Bamdra\ Loom_<version>_amd64.AppImage
```

If the AppImage refuses to run, install FUSE:

```bash
sudo apt install libfuse2
```

### Updating

The app checks for updates at startup. When one is available, a download button appears in the top bar. The update channel is signed — only releases from this repository can install. If a download fails, a dialog will offer to retry or open the releases page directly.

You can also manually download a newer installer and run it; settings and project state are preserved.

### What to do after installing

Open the [English quickstart](docs/en/01-quickstart.md) — five minutes, plain language, no jargon.

---

## 简体中文

### macOS

1. 下载对应芯片的 `.dmg`：
   - Apple Silicon：`Bamdra Loom_<version>_aarch64.dmg`
   - Intel：`Bamdra Loom_<version>_x64.dmg`
2. 打开 dmg，把 **Bamdra Loom** 拖入应用程序文件夹。
3. 第一次打开会提示"未识别的开发者"。在 Finder 里右键 → **打开**，在弹窗里确认即可。系统会记住这次选择。

#### 如果提示"已损坏，无法打开"

我们没有购买 Apple 开发者账号，安装包做的是 ad-hoc 签名而不是公证。如果系统把它标记为"已损坏"（通常是因为文件经过邮件 / 即时通讯 / 浏览器 quarantine），跑一次清除命令即可：

```bash
xattr -cr "/Applications/Bamdra Loom.app"
```

然后再双击打开。

### Windows

1. 下载 `Bamdra Loom_<version>_x64-setup.exe`。
2. 运行安装包。Windows SmartScreen 可能会拦截 —— 点 **更多信息** → **仍要运行**。
3. 跟着安装向导走完即可。

### Linux

#### deb 包（Debian / Ubuntu 系）

```bash
sudo dpkg -i bamdra-loom_<version>_amd64.deb
sudo apt-get install -f
```

#### AppImage

```bash
chmod +x Bamdra\ Loom_<version>_amd64.AppImage
./Bamdra\ Loom_<version>_amd64.AppImage
```

如果 AppImage 无法运行，安装 FUSE：

```bash
sudo apt install libfuse2
```

### 升级

应用启动时会检查更新。新版本可用时，TopBar 上会出现一个下载按钮。更新通道是签名的，只有来自本仓库的 release 才能安装。如果自动下载失败，会弹窗提示你——可以重试，也可以直接到 releases 页手动下载。

也可以手动下载新版安装包覆盖安装，本机设置和项目状态都会保留。

### 装好之后做什么

打开[中文上手指南](docs/zh/01-quickstart.md)——五分钟，大白话，没有术语。
