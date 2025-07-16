# 📦 LocalSend for Kylin OS - Binary Releases

> **专为麒麟系统编译的 LocalSend 二进制发布仓库**

## ⚠️ **重要提示**

如果您在下载时遇到 "没有那个文件或目录" 的错误，请使用以下**正确的下载链接**：

```bash
# 正确的下载命令
wget https://github.com/Oligofornet/new/raw/main/localsend-kylin-x86_64-20250716.tar.gz
```

**注意**：请使用 `/raw/main/` 而不是 `/releases/download/`

[![GitHub release](https://img.shields.io/github/release/Oligofornet/localsend-kylin-releases.svg)](https://github.com/Oligofornet/localsend-kylin-releases/releases)
[![GitHub downloads](https://img.shields.io/github/downloads/Oligofornet/localsend-kylin-releases/total.svg)](https://github.com/Oligofornet/localsend-kylin-releases/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 🎯 **项目简介**

这是 LocalSend 专为麒麟系统（Kylin OS）编译的二进制发布仓库。LocalSend 是一个开源的跨平台文件传输应用，类似于 AirDrop，但支持所有平台。

- **🏠 主项目仓库**: https://github.com/Oligofornet/localsend
- **🎨 品牌**: Oligofornet 定制版本
- **🖥️ 目标系统**: 麒麟 OS (Kylin OS)

## 📥 **快速下载**

### 最新版本：v1.0.0 (2025-07-16)

**文件**: `localsend-kylin-x86_64-20250716.tar.gz`  
**大小**: 22.6 MB  
**架构**: x86_64  
**MD5**: `93ab308efa0ac53a994147e00295db15`

#### 🚀 一键下载安装

```bash
# 下载
wget https://github.com/Oligofornet/new/raw/main/localsend-kylin-x86_64-20250716.tar.gz

# 解压
tar -xzf localsend-kylin-x86_64-20250716.tar.gz

# 进入目录
cd localsend-kylin-x86_64-20250716/

# 安装
sudo ./install.sh
```

#### 📋 其他下载方式

**方法一：使用 wget**
```bash
wget https://github.com/Oligofornet/new/raw/main/localsend-kylin-x86_64-20250716.tar.gz
```

**方法二：使用 curl**
```bash
curl -L -O https://github.com/Oligofornet/new/raw/main/localsend-kylin-x86_64-20250716.tar.gz
```

**方法三：克隆仓库**
```bash
git clone https://github.com/Oligofornet/new.git
cd new/
```

**方法四：浏览器下载**
- 访问：https://github.com/Oligofornet/new
- 点击 `localsend-kylin-x86_64-20250716.tar.gz` 文件
- 点击 "Download" 按钮

**方法五：如果遇到问题**
```bash
# 清理之前的下载
rm -f localsend-kylin-x86_64-20250716.tar.gz
rm -rf localsend-kylin-x86_64-20250716/

# 重新下载
wget https://github.com/Oligofornet/new/raw/main/localsend-kylin-x86_64-20250716.tar.gz

# 验证文件
md5sum localsend-kylin-x86_64-20250716.tar.gz
# 应该显示: 93ab308efa0ac53a994147e00295db15

# 解压并安装
tar -xzf localsend-kylin-x86_64-20250716.tar.gz
cd localsend-kylin-x86_64-20250716/
sudo ./install.sh
```

## 🔧 **系统要求**

- **操作系统**: 麒麟 OS (兼容 Ubuntu 22.04+)
- **架构**: x86_64 (64位 Intel/AMD)
- **图形库**: GTK 3.0+ (麒麟系统预装)
- **内存**: 最少 512 MB RAM
- **存储**: 100 MB 可用空间

## 🚀 **安装方法**

### 方法一：系统安装（推荐）
```bash
sudo ./install.sh
```
- 安装到 `/opt/localsend/`
- 创建桌面快捷方式
- 添加到应用程序菜单
- 创建命令行链接

### 方法二：便携运行
```bash
./localsend
```
- 无需安装，直接运行
- 适合临时使用或测试

### 卸载方法
```bash
sudo ./uninstall.sh
```

## ✨ **版本特性**

### v1.0.0 (2025-07-16)
- 🎨 **全新品牌形象**: Oligofornet 定制 logo 和品牌
- 🖥️ **麒麟系统优化**: 专为麒麟 OS x86_64 架构编译
- 📦 **独立可执行**: 包含所有依赖库，无需额外安装
- 🚀 **一键安装**: 自动化安装和卸载脚本
- 🔗 **桌面集成**: 应用程序菜单和桌面快捷方式支持
- 🌐 **跨平台兼容**: 与其他平台的 LocalSend 完全兼容

## 🔐 **文件验证**

下载后请验证文件完整性：

```bash
# 检查 MD5
md5sum localsend-kylin-x86_64-20250716.tar.gz
# 应该显示: 93ab308efa0ac53a994147e00295db15

# 检查文件大小
ls -lh localsend-kylin-x86_64-20250716.tar.gz
# 应该显示: 22.6M
```

## 🔧 **技术信息**

- **编译日期**: 2025年7月16日
- **Flutter 版本**: 3.24.5
- **Rust 版本**: 1.88.0
- **构建类型**: Release (生产优化)
- **编译环境**: Ubuntu 22.04.5 LTS

## 📖 **使用说明**

1. **启动应用**: 安装后在应用程序菜单中找到 "LocalSend" 或运行 `localsend` 命令
2. **文件传输**: 选择要传输的文件，选择目标设备
3. **接收文件**: 其他设备可以发现并向您发送文件
4. **网络要求**: 确保设备在同一局域网内

## 🐛 **问题反馈**

如遇到问题，请：

1. **检查系统兼容性**: 确认运行在麒麟 OS x86_64 系统上
2. **查看日志**: 运行 `./localsend --verbose` 获取详细日志
3. **提交 Issue**: https://github.com/Oligofornet/localsend/issues
4. **查看文档**: https://github.com/Oligofornet/localsend

## 📜 **许可证**

本项目基于 MIT 许可证发布。详见 [LICENSE](LICENSE) 文件。

## 🙏 **致谢**

- 感谢 [LocalSend](https://github.com/localsend/localsend) 原项目团队
- 感谢麒麟系统社区的支持和反馈

---

**🌟 如果这个项目对您有帮助，请给我们一个 Star！**

**📞 技术支持**: https://github.com/Oligofornet/localsend/issues
