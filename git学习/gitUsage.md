##  git常用操作

### 一、git的结构

历史版本：本地库

临时版本：暂存区

 写代码：工作区

#### 工作流程：

`工作区--> git add --> 暂存区 --> git commit --> 本地库`

### 二、git和代码托管中心

1. 局域网环境下：gitlab
2. 外网：github/码云  

#### 本地库和远程库关系

<img src="C:\Users\Dylan\Desktop\【liubing】所有笔记\git学习\assets\git1.png" style="zoom:33%;" />

<img src="C:\Users\Dylan\Desktop\【liubing】所有笔记\git学习\assets\git2.png" alt="git2" style="zoom:33%;" />



### 三、git命令行操作

1. 本地库初始化

   1. 新建一个文件夹，在新建的文件夹中【GitBash-Here】

   2. git init : 初始化一个空本地仓库  ./git文件夹中存放的是本地库相关的文件和子目录

   3. 设置签名：这里设置的签名和GitHub账户没有任何关系

      1. 项目级别：仅在当前本地库范围内有效

         ```
         git config user.name [username]
         git config user.email [email]
         信息保存地址：./git/config 文件中
         ```

         

      2. 系统用户级别：登录当前操作系统用户范围

         ```
         git config --global user.name [username]
         git config --global user.email [email]
         用户家目录中的 ./gitconfig文件中
         ```

         （优先级：就近原则，项目级别优先于系统级别，二者都有时，采用项目级别）

2. 本地仓库的操作

   1. git status：查看工作区和暂存区的状态
   2. git add . [filename] [ * ]：将工作区的文件提交到暂存区
   3. git commit -m "说明"：将暂存区的内容提交到本地库
   4. git log：查看日志， git reflog：查看日志简要信息
   5. git reset --hard [索引值]
   6. git reset --hard HEAD~n：后退n步且不能撤销
   7. 