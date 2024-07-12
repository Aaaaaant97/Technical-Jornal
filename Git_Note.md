# Git的简单操作（MacOS系统）

## 资源链接

- [廖雪峰官方网站](https://www.liaoxuefeng.com/wiki/896043488029600)
- [CSDN教程](https://blog.csdn.net/qq_36332660/article/details/131024361)

## 主要操作

### 1. 使用 Homebrew 安装 Git

#### 1.1 安装 Homebrew

在终端用户目录中运行以下命令：

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

#### 1.2 安装 Git

在终端用户目录中运行以下命令：

```bash
brew install git
```

### 2. 创建本地版本库

#### 2.1 创建空目录

```bash
mkdir mygit
cd mygit
```

#### 2.2 用Git管理

在该目录下执行：

```bash
git init
```

### 3.创建Github仓库

### 4.链接Github与本地版本库

#### 4.1 创建SSH Key

在用户主目录下，看看有没有 `.ssh`目录，如果有，再看看这个目录下有没有`id_rsa`和`id_rsa.pub`这两个文件，如果已经有了，可直接跳到下一步。如果没有，在用户主目录下创建SSH Key：

```bash
ssh-keygen -t rsa -C "youremail@example.com"
```

其中`youremail@example.com`是注册github的邮箱名。

#### 4.2 复制`id_rsa.pub`内容

进入`.ssh`目录，以下命令可以直接展开`cat id_rsa.pub`中的内容：

```bash
cat id_rsa.pub
```

复制展开的内容。

#### 4.3 在Github中“Add SSH Key”

进入Settings，点Add SSH Key，Title任意，文本框中粘贴`id_rsa.pub`的内容，点"Add Key"。

#### 4.4 关联本地库和Github上的库

在本地的`mygit`目录下执行以下操作，其中：YourGithubName和YourGithubRepoName换成自己的：

```bash
git remote add origin git@github.com:YourGithubName/YourGithubRepoName.git
```

#### 4.5 将本地版本库中的内容推送到Github

第一次推送需要执行以下命令，之后就不用这样：

```bash
git push -u origin main
```
（我的电脑默认是main，有一些可能是master，可以都尝试一下）

### 5.日常简单操作（持续更新...

```bash
git pull
git add xxx.txt
git commit -m "xxxxxx"
git push
```
