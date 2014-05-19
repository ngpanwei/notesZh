上传Eclipse Project到github
==========================

这文件说明如何通过命令行上传一个已有的Eclipse Project到github的repository。
＊ 我假设你已经安装git命令行工具。
＊ 我假设你已经安装Eclipse。

### 创建github repository
目标：通过github网站创建github repository
假设：你已经注册github账号。
游览到你的github账号主页。
````
https://github.com/《账号》
````
#### 1）网页右上角有个“＋”的菜单栏。点击“＋”选择“New repository”
github弹出一个Repository配置页面。
#### 2）输入Repository配置：
````
Repository name ：(repo-name) <-- 你想要的repository名>
Description     ：<-- 给个简单描述
Initialize this repository with a README ：勾选
````
点击"Create Repository"
#### 3) 检查新创建的Repository主页
主页右下角有这个Repository。
在“HTTPS clone URL”标记底下有这个repository入境。
是这个格式的：https://github.com/(username)/(repo-name>.git

### 建立本地Local Repository
目标：通过git命令行工具建立相对的本地Local Repository

#### 1）打开你的git命令行工具。
一打开命令行工具，请查你当前的目录
````
> pwd
````

#### 2）创建本地git的工作目录
创建一个本地的工作目录。
假设你要用“git”作为这个目录名
````
mkdir git
cd git
pwd 
````
记录你的git工作目录入境（path-to-git-working-dir）。

#### 3）Clone github 的 Repository
创建本地的相对repository
````
> git clone https://github.com/(username)/(repo-name>.git
> ls
````
之后你可以看见一个新的创建目录：（repo-name）

### 移植你的已有Eclipse Project到你的本地Repository


### Push你的Eclipse Project到githubRepository





