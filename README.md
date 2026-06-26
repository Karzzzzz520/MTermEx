# MTermEx - 社区维护版

> MT 终端扩展包 - 非官方版 (Termux 环境版)
> 社区维护 fork 自 [ZeroAicy/MTermEx](https://github.com/ZeroAicy/MTermEx)

## 📌 项目简介

MTermEx 是 [MT 管理器](https://mt2.cn/) 的终端扩展包，为 MT 管理器提供 Termux 终端环境支持。

## ✨ 特性

- 基于 Termux 环境构建的终端扩展包
- 集成 bash、busybox 等常用 shell 工具
- 支持多架构（arm64-v8a、armeabi-v7a、x86_64）
- 兼容 Android 5.0 (API 21) 及以上

## 📦 构建

### 环境要求

- JDK 17
- Android SDK (compileSdk 34, buildTools 34.0.0)
- Gradle 8.3.2+

### 构建命令

```bash
git clone https://github.com/Karzzzzz520/MTermEx.git
cd MTermEx
./gradlew assembleDebug    # debug 版本
./gradlew assembleRelease  # release 版本
```

构建产物位于 `app/build/outputs/apk/` 目录。

## 🚀 安装

1. 从 [Releases](https://github.com/Karzzzzz520/MTermEx/releases) 下载最新 APK
2. 在 MT 管理器中安装扩展包
3. 重启 MT 管理器即可使用终端功能

## 🐛 已知问题

- [ ] KernelSU root 权限调用失败 ([#4](https://github.com/ZeroAicy/MTermEx/issues/4))
- [ ] 缺少 native 库编译文档 ([#2](https://github.com/ZeroAicy/MTermEx/issues/2))

## 📝 社区维护说明

本仓库为社区维护版本，原作者 [ZeroAicy (墨凡尘轩)](https://github.com/ZeroAicy) 已同意社区维护。

维护目标：
- 修复已知 Bug
- 升级构建工具链和 SDK 版本
- 提供 Release 版本下载
- 补充文档

## 📄 许可证

本项目基于 [MIT 许可证](LICENSE) 开源。

原作者: [ZeroAicy](https://github.com/ZeroAicy)
