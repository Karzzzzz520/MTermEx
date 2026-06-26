MTermEx 启动脚本 - 社区维护版

工作原理:
1. 扩展包安装后,MT管理器会将 lib 目录的文件释放到应用数据目录
2. sh 文件会被MT管理器调用,它只是转发调用 bash
3. bash 文件是真正的启动脚本,它会:
   - 检测是否有解压好的 termux 环境
   - 如果没有,从 libtermux.so(实际是tar包) 解压
   - 设置 proot 环境变量
   - 启动 proot 进入 termux 环境

文件说明:
- libLoader.so: proot loader
- libproot.so: proot 二进制
- libtermux.so: termux rootfs 压缩包(tar.gz)
- bash: 启动脚本(POSIX shell)
- sh -> bash 的简单转发
- busybox: 多功能工具箱

适配说明:
- MTermEx 包名: bin.mt.termex (不是 com.termux!)
- targetSdk 28: 保留数据目录执行权限
