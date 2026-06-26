# MTermEx - 社区维护版

> MT 终端扩展包 - 非官方版 (Termux 环境版)
> 社区维护 fork 自 [ZeroAicy/MTermEx](https://github.com/ZeroAicy/MTermEx)

## 📌 项目简介

MTermEx 是 [MT 管理器](https://mt2.cn/) 的终端扩展包，为 MT 管理器提供 Termux 终端环境支持。

## 🆕 社区维护版改动

### v3.7 (2026-06-26)

- **[修复] 路径硬编码问题** — 原版所有路径写死为 `com.termux`，现在动态适配 `bin.mt.termex`
- **[修复] targetSdk 降级至 28** — 确保数据目录保留执行权限（MT 官方也提供了 TargetSdk28 版本）
- **[修复] KernelSU 兼容** — 自动检测 KernelSU (`/data/adb/ksu/bin/su`) 路径
- **[新增] 设备文件系统挂载** — proot 增加 `/dev`、`/proc`、`/sys` 绑定
- **[优化] Termux 版本** — 版本信息更新至 0.143.0
- **[新增] GitHub Actions CI/CD** — 自动构建 + 自动发布 Release
- **[新增] MIT 开源许可证**

### 原版问题记录

| 问题 | 状态 | 说明 |
|------|------|------|
| 路径硬编码 `com.termux` | ✅ 已修复 | 动态检测包名路径 |
| targetSdk 30+ 无执行权限 | ✅ 已修复 | 降级 targetSdk 至 28 |
| KernelSU root 调用失败 | ✅ 已修复 | 多路径 su 检测 |
| Termux rootfs 过旧 | ✅ 已修复 | 更新至 0.143.0 |
| 缺少设备挂载 | ✅ 已修复 | 绑定 /dev /proc /sys |
| 缺少编译文档 | 🔧 计划中 | 后续补充 |

## 📦 安装

### 方式一：从 Release 下载

1. 从 [Releases](https://github.com/Karzzzzz520/MTermEx/releases) 下载最新 APK
2. 在 MT 管理器中安装扩展包
3. 重启 MT 管理器即可使用终端功能

### 方式二：本地构建

**环境要求：**
- JDK 17
- Android SDK (compileSdk 35)
- Gradle 8.11.1+

```bash
git clone https://github.com/Karzzzzz520/MTermEx.git
cd MTermEx
./gradlew assembleDebug    # debug 版本
./gradlew assembleRelease  # release 版本
```

构建产物位于 `app/build/outputs/apk/` 目录。

## ⚠️ 重要说明

- **请使用 MT 管理器正式版的 TargetSdk28 版本**，或确认 MT 设置中终端扩展包路径正确
- 本扩展包与 Termux 应用独立，互不影响
- 本扩展包包名为 `bin.mt.termex`，与原版 `com.termux` 完全不同

## 📄 许可证

本项目基于 [MIT 许可证](LICENSE) 开源。

原作者: [ZeroAicy](https://github.com/ZeroAicy)
社区维护: [Karzzzzz520](https://github.com/Karzzzzz520)
