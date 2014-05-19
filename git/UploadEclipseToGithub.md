上传Eclipse Project到github
==========================

这文件说明如何通过命令行上传一个已有的Eclipse Project到github的repository。
＊ 我假设你已经安装git命令行工具。
＊ 我假设你已经安装Eclipse。

这个指导有一系列参数。每个参数是通过(xxx)的格式在这个指导现实。在操作是请替换这个参数。

 Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

| Parameter               | Example | Description |
|----------------------|-----|--|
| project-name         | myproject | a |
| username             | ngpanwei | a|
| repo-name            | myrepo | a|
| git-working-folder   | mygit     |a |
| git-working-path     | /Users/ngpanwei/mygit | a |


### 创建github repository
目标：通过github网站创建github repository
假设：你已经注册github账号。
游览到你的github账号主页。
````
https://github.com/(username)
````
#### 1）网页右上角有个“＋”的菜单栏。点击“＋”选择“New repository”
github弹出一个Repository配置页面。
#### 2）输入Repository配置：
````
Repository name ：<-- 输入你想要的repository名 (repo-name) 
Description     ：<-- 输入给个简单描述
Initialize this repository with a README ：勾选
````
点击"Create Repository"
#### 3) 检查新创建的Repository主页
主页右下角有这个Repository。
在“HTTPS clone URL”标记底下有这个repository入境。
是这个格式的：！
https://github.com/(username)/(repo-name）.git

### 建立本地Local Repository
目标：通过git命令行工具建立相对的本地Local Repository

#### 1）打开你的git命令行工具。
一打开命令行工具，请查你当前的目录
````
> pwd
````

#### 2）创建本地git的工作目录
假设你要用(git-working-folder)作为这个目录名
````
mkdir (git-folder)
cd git
pwd 
````
记录你的git工作目录入境（git-working-path）。

#### 3）Clone github 的 Repository
创建本地的相对repository
````
> git clone https://github.com/(username)/(repo-name).git
> ls
````
之后你可以看见一个新的创建目录:（repo-name）


### 移植你的已有Eclipse Project到你的本地Repository
假设：你已经创建Eclipse Project了而这个Eclipse Project名称是(project-name)

#### 1）通过Eclipse Refactor Move移植Eclipse Project
1) 打开你的Eclipse Project。
1) 鼠标点击Eclipse Project。右键-->Refactor-->Move
1）在Move Project窗口输入
````
Location:(git-working-path)/(project-name)
````
1) 移植之后确认
在你的命令行工具会看到已被移植的Eclipse Project
````
> ls
````

### Add，Commit，Push你的Eclipse Project到github Repository
现在你可以通过命令行把你的Eclipse Project上传到你的github repository
1) 上传Eclpise Project
````
> git add
> git commit -a -m "upload"
> git push origin master
````
1) 验证正确上传
刷新你的github repository。现在应该能够看到你的Eclipse Project了。




