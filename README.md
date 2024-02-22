# MicroMamba Installation Script | [中文](./README_CN.md)
A script for installing and uninstalling MicroMamba, a lightweight Conda alternative that supports both silent and interactive installations.

## Description

This script is used to install and uninstall MicroMamba, a lightweight alternative to Conda. It supports both silent installation (no user interaction required) and interactive installation.

## Installation
The script provides several different ways to use it, including silent installation, interactive installation, and uninstall.

## Silent Installation
Silent installation mode allows you to install MicroMamba without any interaction.

## Default Path Silent Installation
To silently install MicroMamba in the default path ($HOME/micromamba), run:

```shell
./install.sh --silent
```

## Custom Path Silent Installation
If you want to silently install MicroMamba in a custom path, run:

```shell
./install.sh --silent /your/custom/path
# or
bash <(curl -s https://cdn.jsdelivr.net/gh/hotwa/MicroMamba_Installer@main/install.sh) --silent-install
bash <(wget -qO- https://cdn.jsdelivr.net/gh/hotwa/MicroMamba_Installer@main/install.sh) --silent-install
```

Here, /your/custom/path is the custom installation path you chose.

## Interactive Installation
Interactive installation mode will prompt you for the required configuration information.

To start interactive installation, just run the script without any arguments:

```shell
./install.sh
```

Then follow the prompts, choose to install or uninstall, and set the installation path (if you choose to install).

## Uninstalling MicroMamba
The script also provides an option to uninstall MicroMamba. In interactive mode, just choose the uninstall option.

```shell
./install.sh
```

Then choose the uninstall option, follow the prompts, and the uninstall will be completed.

Setting Environment Variables
This script will automatically set the environment variables MICROMAMBA_BIN_PATH and MAMBA_ROOT_PREFIX, and add the MicroMamba alias mba to the user's .bashrc file.

## Usage
This script supports both interactive and silent installation.

## Interactive Installation
Just run the script and follow the prompts:

```shell
./installtest.sh
```

## Silent Installation
Use the --silent-install option to perform a silent installation.

Use the default installation path:

```shell
./installtest.sh --silent-install
```

Use a custom installation path:

```shell
./installtest.sh --silent-install /custom/path/for/micromamba
```

When using a custom path, /custom/path/for/micromamba will be used as the value of MAMBA_ROOT_PREFIX.

## Silent Uninstall
Use the --silent-uninstall option to perform a silent uninstall:

```shell
./installtest.sh --silent-uninstall
```

## Silent Update
Use the --silent-update option to perform a silent update:

```shell
./installtest.sh --silent-update
```

## Adding Conda Channels

```shell
conda config --show channels
conda config --add channels https://mirrors.bfsu.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.bfsu.edu.cn/anaconda/cloud/conda-forge/
conda config --add channels https://mirrors.bfsu.edu.cn/anaconda/cloud/bioconda/
conda config --add channels https://mirrors.aliyun.com/anaconda/cloud/msys2/
conda config --add channels https://mirrors.bfsu.edu.cn/anaconda/cloud/bioconda/
conda config --add channels https://mirrors.bfsu.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.bfsu.edu.cn/anaconda/pkgs/r/
conda config --add channels conda-forge
conda config --add channels bioconda
conda config --add channels r
conda config --set remote_read_timeout_secs 6000.0
```

## Help
To view the usage instructions for the script, run:

```shell
./install.sh --help
```

## Tested Systems

This script has been tested on the following systems:

Debian 12 (Deepin)
