# MicroMamba 安装脚本

## 描述

这个脚本用于安装和卸载 MicroMamba，一个轻量级的 Conda 替代品。它支持静默安装（无需用户交互）和交互式安装。

## 安装

脚本提供了几种不同的使用方式，包括静默安装、交互式安装和卸载。

### 静默安装

静默安装模式允许您在不进行任何交互的情况下安装 MicroMamba。

### 默认路径静默安装

要在默认路径 ($HOME/micromamba) 下静默安装 MicroMamba，运行：

```shell
./install.sh --silent
#或者

echo 1 | bash <(curl -s https://cdn.jsdelivr.net/gh/hotwa/MicroMamba_Installer@main/install.sh)

echo 1 | bash <(wget -qO- https://cdn.jsdelivr.net/gh/hotwa/MicroMamba_Installer@main/install.sh)

```

### 自定义路径静默安装

如果您想在自定义路径下静默安装 MicroMamba，运行：

```shell
./install.sh --silent /your/custom/path
```

在这里，/your/custom/path 是您选择的自定义安装路径。

### 交互式安装

交互式安装模式会提示您输入所需的配置信息。

要开始交互式安装，只需运行脚本而不带任何参数：

```shell
./install.sh
```

然后按照提示操作，选择安装或卸载，以及设置安装路径（如果选择安装）。

## 卸载 MicroMamba

脚本也提供了卸载 MicroMamba 的选项。在交互式模式中，选择相应的卸载选项即可。

```shell
./install.sh
```

然后选择卸载选项，按照提示进行操作即可完成卸载。

### 设置环境变量
此脚本将自动设置环境变量 MICROMAMBA_BIN_PATH 和 MAMBA_ROOT_PREFIX 并在用户的 .bashrc 文件中添加 MicroMamba 的别名 mba。

### 使用方法
此脚本支持交互式和静默两种安装方式。

### 交互式安装
直接运行脚本并按提示操作：

```shell
./installtest.sh
```

### 静默安装
使用 --silent-install 参数进行静默安装。

使用默认安装路径：

```shell
./installtest.sh --silent-install
```

使用自定义安装路径：

```shell
./installtest.sh --silent-install /custom/path/for/micromamba
```

在使用自定义路径时，/custom/path/for/micromamba 将作为 MAMBA_ROOT_PREFIX 的值。

## 静默卸载

使用 --silent-uninstall 参数进行静默卸载：

```shell
./installtest.sh --silent-uninstall
```

## 静默更新

使用 --silent-update 参数进行静默更新：

```shell
./installtest.sh --silent-update
```

## 添加 Conda 源

```shell
conda config --show channels
conda config --add channels https://mirrors.bfsu.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.bfsu.edu.cn/anaconda/cloud/conda-forge/
conda config --add channels https://mirrors.bfsu.edu.cn/anaconda/cloud/bioconda/
conda config --add channels https://mirrors.aliyun.com/anaconda/cloud/msys2
conda config --add channels https://mirrors.aliyun.com/anaconda/cloud/bioconda
conda config --add channels https://mirrors.aliyun.com/anaconda/pkgs/main
conda config --add channels https://mirrors.aliyun.com/anaconda/pkgs/r
conda config --add channels conda-forge
conda config --add channels bioconda
conda config --add channels r
conda config --set remote_read_timeout_secs 6000.0
```

## 帮助

要查看脚本的用法说明，请运行：

```shell
./install.sh --help
```

测试系统
此脚本已在以下系统上进行测试：

Debian 12 (Deepin)
