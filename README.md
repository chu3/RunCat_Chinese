![效果图](https://s3.bmp.ovh/imgs/2024/03/21/0f8fad206b7680b6.png)

# 🐱 macOS RunCat 中文语言包

> 当前适配 RunCat 版本：12.0

为 macOS App Store 应用 [RunCat](https://apps.apple.com/cn/app/runcat/id1429033973?mt=12) 提供中文语言支持。通过自动/手动替换应用资源文件实现汉化。

## 🚀 一键自动安装（命令行方式）

如果你更习惯使用终端，可以通过下面一行命令自动安装中文语言包。该命令会使用 sudo 权限拉取 Git 仓库，并将仓库中缺失的文件添加到 `/Applications/RunCat.app/Contents` 中：

```bash
sudo bash -c 'tmp_dir=$(mktemp -d) && git clone https://github.com/chu3/RunCat_Chinese.git "$tmp_dir" && rsync -av --ignore-existing "$tmp_dir/Contents/" "/Applications/RunCat.app/Contents/" && rm -rf "$tmp_dir"'
```

**注意：**

-   请确保你拥有 sudo 权限。
-   该命令依赖 Git 和 rsync 工具，请确保它们已安装在系统中。

## 🖥️ 手动安装方法

1. 下载中文语言包中的 `Contents` 文件夹。
2. 打开 Finder，右键点击 RunCat 应用程序，选择“显示包内容”。
3. 将下载的 `Contents` 文件夹与安装目录中的同名文件夹进行 **合并**  
   **（建议：先拷贝再粘贴，避免直接拖拽导致无法合并）**。
4. 重新启动 RunCat 应用程序。

## 💾 离线安装包

1. 下载 [Releases](https://github.com/chu3/RunCat_Chinese/releases) 中的 RunCat.zip 文件，并解压缩。
2. 将解压后的 RunCat 应用程序拖放到“应用程序”文件夹中，打开即可使用。

如果显示 **"RunCat" 已损坏，无法打开**，请前往【系统设置...】-【隐私与安全性】-【安全性】，找到 “已阻止使用 ‘RunCat’，因为来自身份不明的开发者。” 并点击【仍要打开】。

## 🎛️ 版本选择

不同版本界面差异较大，可以根据个人喜好在 [Releases](https://github.com/chu3/RunCat_Chinese/releases)页面中选择合适的版本下载安装。

## 📦 更新维护

建议 Star 本项目以获取更新通知，后续更新只需重新执行安装命令即可。

## 🤝 贡献指南

欢迎通过 Issue 反馈问题或提交 Pull Request 参与汉化维护。
