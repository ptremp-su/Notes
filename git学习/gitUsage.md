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

<img src="https://github.com/ptremp-su/Notes/blob/master/git%E5%AD%A6%E4%B9%A0/assets/git1.png" style="zoom:33%;" />

<img src="https://github.com/ptremp-su/Notes/blob/master/git%E5%AD%A6%E4%B9%A0/assets/git2.png" alt="git2" style="zoom:33%;" />



### 三、git命令行操作【git --help】

1. **本地库初始化**

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

2. **本地仓库的操作**

   ```
   git status：查看工作区和暂存区的状态
   git add . [filename] [ * ]：将工作区的文件提交到暂存区
   git commit -m "说明"：将暂存区的内容提交到本地库
   git log：查看日志， git reflog：查看日志简要信息
   git reset --hard [索引值]
   git reset --hard HEAD~n：后退n步且不能撤销
   git diff [文件名]：将工作区中的文件和暂存区的文件进行比较
   git diff [本地库中历史版本]：将工作区中的文件和历史版本比较
   git diff：比较多个版本
   ```

3. **分支管理**

   ```
   git branch -v:查看现在所有的分支
   git branch [分支名字]:创建新的分支
   git checkout [分支名]:切换分支
   //合并分支第一步，切换到接受修改(合并)的分支
   //第二步，执行merge
   git merge [分支名1]:将分支名1合并到当前所在的分支
   
   
   ```

   

