+++
title = "Lab 1: 实验开发环境安装"
weight = 10
+++

## 1. 实验环境概览
本次实验课程为动手开发系列，因此需要建立完整的开发环境用于完成整个Azure IoT解决方案的开发，为简化开发环境的配置，我们尽量选择跨平台和支持插件的开发工具和环境，主要包括：
* **开发PC**：可以使用您的本地机器或者在Azure上的虚拟机，课程将以Azure虚拟机为例说明。
* **操作系统**：本次实验所用到的开发工具和依赖库均支持跨平台开发，因此您可以使用Windows, Linux或Mac OS来完成本次实验过程。本节作为开发环境安装说明，将以Windows环境为例说明实验所需要的开发工具和依赖库的安装，其他操作系统环境下的安装请参照文末所附文档进行安装。

* **开发工具**：Visual Studio Code和Azure CLI将作为本次实验的主要开发工具，二者均支持用于完成本次实验的一系列扩展工具。
* **开发语言**：本次课程的实验项目主要包括边缘端设备应用和服务端应用开发，采用的开发语言包括：
    * 边缘端设备应用： Python 3.8或以上。
    * 服务端应用：Java，基于JDK 11和Spring Boot。
    * 前端应用：Javascript。
## 2. 开发工具
* Maven & JDK 11 or 17
    下载Maven，右键解压，将解压目录apache-maven-3.8.6拷贝到C:\Program Files目录下，并将bin文件夹路径添加到PATH环境变量（win + R, 输入sysdm.cpl）
    下载安装[JDK](https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.5_8.msi)

* 安装Visual Studio Code
* 安装Visual Studio Code 扩展  
    在VSCode中同时按下Ctrl+Shift+`打开VSCode的终端窗口，执行以下命令安装所需的扩展：  
    ```bash
    code --install-extension vscjava.vscode-java-pack
    code --install-extension ms-azuretools.vscode-azurefunctions
    ```

    重启VSCode
* Azure Functions Core Tools  (Azure Functions本地调试需要)   
    [链接](https://learn.microsoft.com/en-us/azure/azure-functions/functions-run-local?tabs=v4%2Cwindows%2Cjava%2Cportal%2Cbash#v2)

    启动Azure Functions本地调试：  
    ```
    func host start
    ```

