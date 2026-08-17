# PeerJS 通信节点v5 - Android APK 自动构建仓库

这是一个使用 **PeerJS (WebRTC)** 的去中心化/点对点通信应用，并通过 **GitHub Actions** 自动化打包构建为 Android APK 安装包。

## 📱 应用信息
- **应用名称**: `PeerJS 通信节点v5`
- **包名 (Package ID)**: `com.p2p.peerjsnode`
- **版本**: `5` (Code: 1)
- **核心技术**: HTML5 / JavaScript / WebRTC / PeerJS / Capacitor

---

## 🚀 如何在 GitHub 上生成 APK

### 第一步：创建 GitHub 仓库
1. 在 GitHub 上新建一个仓库（例如 `peerjs-android-app`）。
2. 将本目录所有文件上传（Push）至该 GitHub 仓库的 `main` 分支。

### 第二步：自动化编译
- 只要向 `main` 分支提交代码，GitHub Actions 会**自动开始云端编译**。
- 也可以在仓库页面的 **Actions** 标签页中，点击 **Build Android APK** -> **Run workflow** 手动触发。

### 第三步：下载 APK
1. 进入 GitHub 仓库顶部的 **Actions** 标签页。
2. 点击最近一次运行成功的任务（绿色对勾）。
3. 滚动到页面底部的 **Artifacts (构建产物)** 区域。
4. 点击 **`PeerJS 通信节点v5-v5-debug-apk`** 即可下载生成的安装包（ZIP包内含 `app-debug.apk`）。
5. 发送到手机即可直接安装运行！

---

## 📂 项目结构
```
├── .github/
│   └── workflows/
│       └── build-apk.yml       # GitHub Actions 自动化编译工作流
├── www/
│   └── index.html              # PeerJS 二合一客户端/服务器核心代码
├── capacitor.config.json       # Capacitor 跨平台容器配置
├── package.json                # 项目依赖清单
└── README.md                   # 本说明文件
```

## 🛠️ 本地调试（可选）
如果您安装了 Android Studio，也可以在本地调试：
```bash
npm install
npx cap add android
npx cap open android
```
