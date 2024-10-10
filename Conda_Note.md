# 用Conda管理环境

## 安装Miniconda(MacOS M芯片架构)

- 下载miniconda installer(gpt tells me)

  ```bash
  curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh
  ```

- 运行installer
  
  ```bash
  bash Miniconda3-latest-MacOSX-arm64.sh
  ```

- 初始化miniconda
  
  ```bash
  source ~/miniconda3/bin/activate
  conda init
  ```

## 创建环境

  ```bash
  conda create --name myenv 
  ```

## 激活环境

  ```bash
  conda activate myenv
  ```

## 退出当前环境

  ```bash
  conda deactivate
  ```

## 设置下载channel

  ```bash
  conda config --add channels conda-forge
  conda config --set channel_priority strict
  ```

## 下载包

  ```bash
  conda install python...
  ```
