# 一、安装所需环境

## 1.Git

### 下载地址

[Git - Install for Windows](https://git-scm.com/install/windows)

### 选择对应版本下载

![图片](photo/001.png)

运行安装程序，使用默认设置（直接点击下一步即可）

### 验证Git安装

按win+R键，调出“运行”，输入cmd回车，输入
```md
git --version
```

输出结果如下即可（版本号可以不同）

![图片](photo/002.png)

## 2.安装 uv（Python 包管理器）

uv 是一个极速的 Python 包管理器和项目管理工具，N.E.K.O 项目推荐使用它来管理依赖。
重要： uv 可以自动安装和管理 Python 版本，因此无需先手动安装 Python。

### 安装方式

#### 方式1：在 PowerShell 中运行

```md
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

#### 方式2：手动安装

##### 先去下载对应版本的uv

下载地址：[https://github.com/astral-sh/uv/releases](https://github.com/astral-sh/uv/releases)
找到你需要的版本（通常选最新的稳定版即可）

##### 下载 Windows ZIP 包

在 Assets 部分，找到文件名类似 uv-0.8.12-x86_64-pc-windows-msvc.zip的压缩包，点击下载（前提是 x86_64-pc-windows-msvc架构，不同架构下载其他版本）

![图片](photo/003.png)

##### ​手动解压

下载完成后，右键点击下载的 .zip文件 -> 属性​ -> 在“常规”选项卡底部，检查是否有“此文件来自其他计算机，可能被阻止以帮助保护该计算机”的提示。如果有，勾选“解除锁定” -> 应用 -> 确定。然后解压 ZIP 文件（可以使用系统自带的解压功能或 7-Zip 等工具）。

##### 放置 uv.exe

将解压出来的 uv.exe文件复制到你希望安装的位置。常见选择有：你的项目目录（方便项目特定使用）。一个专门存放工具的目录（例如 C:\Users\<你的用户名>\bin）。系统 PATH包含的目录（例如 C:\Windows\System32，但通常不推荐放这里）。

##### 添加到 PATH  

搜索“编辑系统环境变量” -> 打开 -> 点击“环境变量”按钮。在“系统变量”或“用户变量”中找到 Path变量-> 编辑。点击“新建”，输入你放置 uv.exe的完整目录路径（例如 C:\Users\<你的用户>\bin）。
一路点击确定保存更改。

#### 验证安装

打开一个新的 PowerShell 或 CMD 窗口，运行

```plaintext
uv --version
```

如果看到版本号输出（如 uv 0.8.12），说明安装成功（如下图所示）

![图片](photo/004.png)

## 3.安装代码编辑器

### Visual Studio Code（推荐）

1. 访问[Visual Studio Code - The open source AI code editor](https://code.visualstudio.com/)

2. 下载并安装

3. 安装推荐扩展：Python、Pylance、GitLens、ESLint（前端开发需要）、Prettier（代码格式化）

### Trae CN（AI 辅助编程）

Trae CN是国内免费的基于 VS Code 的 AI 辅助编程编辑器

1. 访问[立即下载 | TRAE - The Real AI Engineer](https://www.trae.cn/ide/download)下载对应系统的安装包

2. 运行安装程序完成安装

3. Trae CN 内置了 AI 功能，无需额外配置即可使用

提示：Trae CN 与 VS Code 使用相同的扩展系统，上述 VS Code 的推荐扩展同样适用于 Trae CN

### Cursor（AI 辅助编程）

Cursor 是基于 VS Code 的 AI 辅助编程编辑器，非常适合 AI 项目开发：

1. 访问[Download](https://cursor.com/en-US/download)下载对应系统的安装包

2. 运行安装程序完成安装

3. Cursor 内置了 AI 功能，无需额外配置即可使用

提示： Cursor 与 VS Code 使用相同的扩展系统，上述 VS Code 的推荐扩展同样适用于 Cursor

# 二、拉取GitHub上的代码

## 方式1：使用GitHub Desktop（适合新手）

### 注册 GitHub 账号

1. 访问[https://github.com/](https://github.com/)

2. 点击 "Sign up" 注册账号

3. 完成邮箱验证

### 下载GitHub Desktop

下载地址：[Download GitHub Desktop](https://desktop.github.com/download/)
安装打开如图

![图片](photo/005.png)

软件汉化：[https://github.com/robotze/GithubDesktopZhTool/releases/tag/3.5.4](https://github.com/robotze/GithubDesktopZhTool/releases/tag/3.5.4)
下载汉化软件并且解压，再按照图示依次点击

![图片](photo/006.png)

汉化成功图示

![图片](photo/007.png)

### Fork（复刻）N.E.K.O.仓库

进入N.E.K.O.仓库，地址：[GitHub - Project-N-E-K-O/N.E.K.O: N.E.K.O., an AI-native metaverse that nurtures digital creatures and yearns to understand, connect, and grow with us.](https://github.com/Project-N-E-K-O/N.E.K.O)
点击Fork

![图片](photo/008.png)

![图片](photo/009.png)

注意：如果出现Fork的所有者不能是自己，那么一定是你已经Fork此仓库过了
创建完成如图

![图片](photo/010.png)

关闭GitHub Desktop重新启动
点击“克隆存储库”

![图片](photo/011.png)
![图片](photo/012.png)

注意：由于克隆可能存在网络访问问题，推荐开启VPN后下载，或者通过加速地址[GitHub 文件加速代理](https://gh-proxy.com/)使用URL克隆
克隆成功后会如图，点击确定即可

![图片](photo/013.png)

最终界面如图所示

![图片](photo/014.png)

## 方式2：使用Git（待写）

# 三、启动调试服务器

### 启动服务器

在项目根目录下，需要启动以下服务器（建议在不同的终端窗口中分别运行）：

#### 启动Memory Server（记忆服务器）

```plaintext
# 确保在项目根目录下
uv run python memory_server.py
```

#### 启动Main Server（主服务器）

```plaintext
# 在新的终端窗口中，确保在项目根目录下
uv run python main_server.py
```

#### 启动Agent服务器（可选，非必须）

```plaintext
# 在新的终端窗口中，确保在项目根目录下
uv run python agent_server.py
```

提示：
- 如果已激活虚拟环境，可以直接使用python命令代替uv run python
- Memory Server默认运行在端口48912
- 主服务器默认运行在端口48911
- Agent Server（如果启动）默认运行在端口48915

#### 访问Web界面

启动主服务器后，在浏览器中访问：

```plaintext
http://localhost:48911
```

首次访问需要配置API Key，可以在Web界面中完成配置。

# 四、更新代码以及修改、提交、推送、更改(以VScode为例)

## 更新代码

当你接取一个任务后，首先进入自己的Fork仓库检查自己的Fork仓库是否需要更新，点击“Sync fork”
如果如图所示，则说明你Fork的库已经是最新的，不需要更新

![图片](photo/015.png)

如果不是，说明你Fork的库需要更新

## 修改代码

点击在“Visual Studio Code中打开”即可修改代码

![图片](photo/016.png)

在Visual Studio Code中打开后如图

![图片](photo/017.png)

## 推送代码

当你将修改后的代码全部保存后，打开GitHub Desktop，GitHub Desktop会显示所有你修改过与原来代码不一样的地方，示例如图

![图片](photo/018.png)

暂存自己的修改，如图

![图片](photo/019.png)

最后点击推送，即可将代码推送到自己Fork的库（建议提前打开VPN防止因为网络问题失败），如图

![图片](photo/020.png)

这个时候打开自己的GitHub网站查看自己Fork的库，会显示自己的提交，示例如图

![图片](photo/021.png)

## 提交代码至N.E.K.O.

如果确定并且测试过修改过后的代码可行，将代码推送到自己Fork的仓库，则如图

![图片](photo/022.png)

![图片](photo/023.png)

这样你的代码就会被提交给N.E.K.O.的代码库，且可在N.E.K.O.的库的此处查看，如图示例

![图片](photo/024.png)

## 更改提交代码

提交成功后你所提交的更改会被coderabbitai AI审查（以下简称喵老师）

![图片](photo/025.png)

喵老师会对你提交的代码进行审查，如图所示

![图片](photo/026.png)

如果喵老师最后评论结果如图，恭喜，你的代码是可行的，只需要等待Wehos博士最终确认合并即可

![图片](photo/027.png)

如果喵老师最后评论结果是这样的，那么很可惜，你需要修改你的代码

![图片](photo/028.png)

决定你是否需要修改你的代码，主要看Actionable comments posted是否大于0
这时，你需要打开GitHub Desktop，

如果显示当前分支的分支名后有#加上数字（如图示例，不一定是180），不需要更改分支

![图片](photo/029.png)

如果没有，进行图示操作

![图片](photo/030.png)

最终如图

![图片](photo/031.png)

重新安装修改代码、推送代码的步骤来即可，不需要再次提交