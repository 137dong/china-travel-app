# 华夏全景 - 中国旅游指南

一个功能完备的中国旅游应用，支持 Windows (.exe)、Android (.apk)、iOS (.ipa) 三平台。

## 📱 功能特性

- 🗺️ 交互式中国地图（高德地图，国内秒加载）
- 🏛️ 34个省级行政区 + 176+个景点全覆盖
- 🌤️ 实时天气（Open-Meteo API）
- 🚄 交通查询（高铁/飞机/大巴）
- 🔍 全局搜索
- 📋 景点详情（门票/时间/贴士）

## 📦 已打包文件

| 平台 | 文件 | 大小 |
|------|------|------|
| Windows | `electron-app/dist/华夏全景.exe` | 14MB |
| Android | 通过 GitHub Actions 构建 | - |
| iOS | 通过 GitHub Actions 构建 | - |

## 🚀 构建 Android APK

### 方式一：GitHub Actions（推荐，免费）

1. 将本目录推送到 GitHub 仓库
2. 进入 Actions → Build Android APK
3. 点击 "Run workflow"
4. 等待构建完成，下载 APK

### 方式二：本地构建（需要 Android Studio）

```bash
cd android
./gradlew assembleDebug
```

APK 输出路径：`android/app/build/outputs/apk/debug/app-debug.apk`

## 🍎 构建 iOS IPA

### 方式一：GitHub Actions（需要 Apple Developer 账号）

1. 将本目录推送到 GitHub 仓库
2. 配置 Secrets：`APPLE_DEVELOPER_CERTIFICATE`、`APPLE_DEVELOPER_PASSWORD`
3. 进入 Actions → Build iOS IPA
4. 点击 "Run workflow"

### 方式二：本地构建（需要 macOS + Xcode）

```bash
cd ios
xcodebuild -project ios.xcodeproj -scheme ios -configuration Release archive
```

## 🌐 在线使用

直接浏览器打开 `travel-app.html` 即可使用。

## 📝 技术栈

- 前端：HTML5 + CSS3 + JavaScript（Leaflet.js 地图）
- 桌面：PyInstaller + pywebview
- 移动端：Android WebView / iOS WKWebView
- 构建：GitHub Actions CI/CD
