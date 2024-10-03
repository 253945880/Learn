<!-- markdownlint-disable MD033 MD041 -->
<p align="center">
  <img alt="LOGO" src="https://cdn.jsdelivr.net/gh/MaaAssistantArknights/design@main/logo/maa-logo_512x512.png" width="256" height="256" />
</p>

<div align="center">

# MMAA-DNFaides

</div>

本仓库为 [MaaFramework](https://github.com/MaaXYZ/MaaFramework) 所提供的项目模板简单改写，

> **MaaFramework** 是基于图像识别技术、运用 [MAA](https://github.com/MaaAssistantArknights/MaaAssistantArknights) 开发经验去芜存菁、完全重写的新一代自动化黑盒测试框架。
> 低代码的同时仍拥有高扩展性，旨在打造一款丰富、领先、且实用的开源库，助力开发者轻松编写出更好的黑盒测试程序，并推广普及。

## 适配情况
    目前仅适配了 1920x1080 480dpi 分辨率

## 使用说明
    以 Windows 用户为主，其他系统请照葫芦画瓢。

    1.使用前，下载DNF助手APP和QQ
    2.在模拟器上安装并登录DNF助手APP
    3.首次使用，打开模拟器，双击打开 MaaPiCli.exe 或 通过 CMD 执行 MaaPiCli.exe
    4.选择ADB（本教程以 Auto detect 为例）
    5.等待扫描设备（设备越多等待时间越长）
    6.选择需要连接的设备
    7.开始使用吧！

    添加 -d 参数可跳过交互直接运行任务，如 ./MaaPiCli.exe -d

    新建一个文本文件，在其中填入以下内容

    ```bash
@echo off
cd D:\MAA-DNFaides\install
MaaPiCli.exe -d
    ```
    
    注意：D:\MAA-DNFaides\install 请替换成你自己的 MAS 目录

    将文本文件重命名为 finish.bat


## 即刻开始

- [⭐ 开发思路](https://github.com/MaaXYZ/MaaFramework/blob/main/docs/zh_cn/0.1-%E5%BC%80%E5%8F%91%E6%80%9D%E8%B7%AF.md)
- [📄 资源准备](https://github.com/MaaXYZ/MaaFramework/blob/main/docs/zh_cn/1.1-%E5%BF%AB%E9%80%9F%E5%BC%80%E5%A7%8B.md)
- [🎞️ 视频教程](https://www.bilibili.com/video/BV1yr421E7MW)

## 如何开发

0. 使用右上角 `Use this template` - `Create a new repository` 来基于本模板创建您自己的项目。

1. 完整克隆本项目及子项目

    ```bash
    git clone --recursive https://github.com/Kagura-wei/MAA-DNFaides.git
    ```
     
    **请注意，一定要完整克隆子项目，不要漏了 `--recursive`，也不要下载 zip 包！** 这步未正确操作会导致所有 OCR（文字识别）失败！

2. 下载 MaaFramework 的 [Release 包](https://github.com/MaaXYZ/MaaFramework/releases)，解压到 `deps` 文件夹中。

3. 配置资源文件。

    ```bash
    python ./configure.py
    ```

4. 按需求修改 `assets` 中的资源文件，请参考 MaaFramework 相关文档。

    - 可使用 [MaaDebugger](https://github.com/MaaXYZ/MaaDebugger) 进行调试；
    - 也可以在本地安装后测试：

        1. 执行安装脚本

            ```bash
            python ./install.py
            ```

        2. 运行 `install/MaaPiCli.exe`

5. 完成开发工作后，上传您的代码并发布版本。

    ```bash
    # 配置 git 信息（仅第一次需要，后续不用再配置）
    git config user.name "您的 GitHub 昵称"
    git config user.email "您的 GitHub 邮箱"
    
    # 提交修改
    git add .
    git commit -m "XX 新功能"
    git push origin HEAD -u
    ```

6. 发布您的版本

    需要先修改仓库设置 `Settings` - `Actions` - `General` - `Read and write permissions` - `Save`

    ```bash
    # CI 检测到 tag 会自动进行发版
    git tag v1.0.0
    git push origin v1.0.0
    ```
