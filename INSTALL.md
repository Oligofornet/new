# 📋 LocalSend for Kylin OS - 安装指南

## 🚀 **快速安装**

### 一键安装脚本

```bash
# 下载并安装
wget https://github.com/Oligofornet/localsend-kylin-releases/releases/download/v1.0.0/localsend-kylin-x86_64-20250716.tar.gz
tar -xzf localsend-kylin-x86_64-20250716.tar.gz
cd localsend-kylin-x86_64-20250716/
sudo ./install.sh
```

## 📋 **详细安装步骤**

### 第一步：下载文件

选择以下任一方式下载：

```bash
# 方式1: 使用 wget
wget https://github.com/Oligofornet/localsend-kylin-releases/releases/download/v1.0.0/localsend-kylin-x86_64-20250716.tar.gz

# 方式2: 使用 curl
curl -L -O https://github.com/Oligofornet/localsend-kylin-releases/releases/download/v1.0.0/localsend-kylin-x86_64-20250716.tar.gz

# 方式3: 浏览器下载
# 访问: https://github.com/Oligofornet/localsend-kylin-releases/releases
```

### 第二步：验证文件

```bash
# 检查文件大小
ls -lh localsend-kylin-x86_64-20250716.tar.gz

# 验证 MD5 校验和
md5sum localsend-kylin-x86_64-20250716.tar.gz
# 应该显示: 93ab308efa0ac53a994147e00295db15
```

### 第三步：解压文件

```bash
tar -xzf localsend-kylin-x86_64-20250716.tar.gz
cd localsend-kylin-x86_64-20250716/
```

### 第四步：选择安装方式

#### 方式A：系统安装（推荐）

```bash
sudo ./install.sh
```

**安装后的效果**：
- ✅ 程序安装到 `/opt/localsend/`
- ✅ 在应用程序菜单中出现 "LocalSend"
- ✅ 可以通过命令行运行 `localsend`
- ✅ 创建桌面快捷方式

#### 方式B：便携运行

```bash
./localsend
```

**适用场景**：
- 临时使用
- 测试运行
- 不想修改系统

## 🔧 **安装后配置**

### 启动应用

```bash
# 命令行启动
localsend

# 或在应用程序菜单中找到 "LocalSend"
```

### 防火墙配置

LocalSend 需要网络权限，可能需要配置防火墙：

```bash
# 允许 LocalSend 通过防火墙（如果使用 ufw）
sudo ufw allow from 192.168.0.0/16 to any port 53317
sudo ufw allow from 10.0.0.0/8 to any port 53317
```

### 网络配置

确保设备在同一局域网内，LocalSend 使用以下端口：
- **发现端口**: 53317 (UDP)
- **传输端口**: 动态分配

## 🗑️ **卸载方法**

### 如果使用系统安装

```bash
sudo /opt/localsend/uninstall.sh
```

### 手动卸载

```bash
# 删除程序文件
sudo rm -rf /opt/localsend/

# 删除桌面文件
sudo rm -f /usr/share/applications/localsend.desktop

# 删除命令行链接
sudo rm -f /usr/local/bin/localsend

# 更新桌面数据库
sudo update-desktop-database /usr/share/applications
```

## 🔍 **故障排除**

### 常见问题

#### 1. 权限错误
```bash
# 确保有执行权限
chmod +x localsend
chmod +x install.sh
```

#### 2. 依赖库缺失
```bash
# 安装 GTK 依赖（通常麒麟系统已预装）
sudo apt update
sudo apt install libgtk-3-0 libayatana-appindicator3-1
```

#### 3. 无法发现其他设备
- 检查防火墙设置
- 确认在同一网络
- 重启应用程序

#### 4. 启动失败
```bash
# 查看详细错误信息
./localsend --verbose

# 检查系统兼容性
ldd localsend_app
```

### 获取帮助

如果遇到问题：

1. **查看日志**: 运行 `./localsend --verbose`
2. **检查系统**: 确认运行在麒麟 OS x86_64 上
3. **提交问题**: https://github.com/Oligofornet/localsend/issues
4. **查看文档**: https://github.com/Oligofornet/localsend

## 📊 **系统要求检查**

运行以下命令检查系统兼容性：

```bash
# 检查架构
uname -m
# 应该显示: x86_64

# 检查操作系统
cat /etc/os-release
# 应该包含麒麟系统信息

# 检查 GTK 版本
pkg-config --modversion gtk+-3.0
# 应该显示 3.x.x 版本
```

---

**🎉 安装完成后，您就可以开始使用 LocalSend 进行文件传输了！**
