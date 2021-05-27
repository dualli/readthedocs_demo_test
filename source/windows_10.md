# Windows 10 软件环境

## 可用的包管理工具

chocolatey 软件数量多,自动配置环境变量；可选portable或安装包安装，如安装 git 可以选择 git.install 或者 git.portable；进阶来说，因为采用安装包的形式安装，choco 提供对安装包的控制，比如安装位置，比如 Everything 可以选择是否以服务形式安装，之类。

scoop 不需要管理员权限；只能便携(portable)安装；

## 安装chocolatey
参考[CHOCOLATEY SETUP/INSTALL](https://docs.chocolatey.org/en-us/choco/setup#more-install-options)
1. 以管理员身份运行cmd
2. 安装
```
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "[System.Net.ServicePointManager]::SecurityProtocol = 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
```
3. 安装图形界面`choco install chocolateygui`

## 安装软件
```
# 日常软件
choco install --yes tim tencentmeeting firefox chrome easyconnect vlc everything teamviewer vscode notepadplusplus winrar FoxitReader nutstore netease-cloudmusic 
# 开发软件
choco install --yes git docker-desktop winscp mobaxterm winscp pycharm eclipse-jee-luna eclipse-cpp dbeaver nodejs cmake make
choco install --yes mariadb jdk8 StrawberryPerl
# 科研软件
choco install --yes zotero anaconda3 Ghostscript qgis
# 文档软件
choco install --yes pandoc 
```

## 常用命令
```
choco install bazel --version 0.17.2
choco uninstall winscp     # 卸载应用
choco list --local         # 查看本地已安装应用
choco outdated             # 检查应用更新
choco upgrade --yes winscp # 升级应用
choco upgrade --yes all    # 升级所有程序
choco info tim             # 查看程序的详细信息
```

## 没有在 Chocolatey 上提供的软件
QQ
微信
有道词典
搜狗输入法
anyconnect
visual studio
office
CAJViewer
gmt
hp打印机驱动
Mapinfo
matlab
百度网盘

## 需要指定版本的软件
cuda

