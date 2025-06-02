# Email Sender

一个跨平台的批量邮件发送应用程序。

## 功能特点

- 支持批量发送邮件
- 可自定义邮件模板
- 支持HTML和纯文本格式
- 自动保存配置和发送记录
- 支持暂停/继续发送功能
- 实时显示发送进度和状态
- 自定义发件人名称
- 跨平台支持（Windows、MacOS、Linux、Android）

## 系统要求

- Python 3.8 或更高版本
- 操作系统：Windows、MacOS、Linux、Android（通过Termux）
- 依赖包：
  - pillow: 图像处理
  - requests: 网络请求
  - html2text: HTML转换
  - configparser: 配置文件处理

## 安装依赖

```bash
pip install -r requirements.txt
```

## 构建可执行文件

### Windows
```bash
python build.py
```

### MacOS/Linux
```bash
python3 build.py
```

### Android (通过Termux)
1. 安装Termux
2. 在Termux中执行：
```bash
pkg update && pkg upgrade
pkg install python git
git clone https://github.com/seaoss/sender.git
cd EmailSender
pip install -r requirements.txt
python pysender.py
```

## 使用说明

### 基本设置
1. 运行程序后，首先配置SMTP服务器信息：
   - SMTP服务器地址（如：smtp.gmail.com）
   - 用户名（邮箱地址）
   - 密码（邮箱授权码）

### 发送邮件
1. 在主界面填写：
   - 收件人邮箱地址（支持多个，每行一个）
   - 邮件主题
   - 邮件正文（支持HTML格式）
   - 发送时间间隔（秒）
   - 发件人显示名称（可选）
2. 选择内容类型（HTML/纯文本）
3. 点击"发送"按钮开始发送
4. 可随时点击"暂停"按钮暂停发送
5. 发送过程中可实时查看进度和状态

## 配置文件说明

### email_settings.ini
邮件基本配置：
- To: 收件人列表
- Subject: 邮件主题
- TextBody: 邮件正文
- Language: 内容类型
- Interval: 发送间隔
- SenderName: 发件人名称

### smtp_settings.ini
SMTP服务器配置：
- Server: 服务器地址
- Username: 用户名
- Password: 密码

### email_cache.json
发送记录缓存：
- 已发送的邮件记录
- 当前发送任务状态
- 暂停时的进度信息

## 注意事项

1. 首次运行时会自动创建必要的配置文件
2. 请确保SMTP服务器配置正确
3. 建议在正式发送前先进行测试
4. 使用HTML格式时，确保内容符合HTML规范
5. 发送大量邮件时，注意控制发送间隔
6. 定期检查发送状态和错误日志

## 支持与反馈

如有问题或建议，请联系：team@seaoss.com

## 赞助支持

如果您觉得这个工具有帮助，欢迎通过程序中的"Sponsor Us"按钮赞助支持我们的开发工作。
