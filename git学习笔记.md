> #### 安装Git（Windows）

从[https://git-for-windows.github.io](https://git-for-windows.github.io/)下载git进行安装，然后桌面右键点击找到git bash here，点击。要是蹦出一个类似于命令行窗口的东西，则说明安装成功。
然后进行一系列设置，在命令行输入：
<code> git config --global user.name "Your Name"
&nbsp;$ git config --global user.email "email@example.com"</code>

> #### 创建仓库并从git bash上传文件到本地仓库

1. 首先选择一个合适的地方，创建一个空目录。
<code> 
mkdir learngit
cd learngit
pwd
</code>
pwd命令用于显示当前目录。

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2567968-c8c61fc0c4054651.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

2. 通过git init命令可以管理仓库。
这样就创建好了一个仓库，这是此目录下会出现一个.git文件，不能进行修改，否则会破坏仓库，也有可能隐藏，隐藏的话在命令行输入ls -ah命令就会出现。

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2567968-14653710abba8798.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

3. 如何通过git创建一个.md文件？

git bash里touch xxx.md或vim xxx.md ，创建的文件位于git bash打开的位置。

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2567968-13a8742c853832fa.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

4.如何将文件上传到仓库？
第一步，用git add命令告诉git添加文件。

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2567968-54df08e44fd6d7ff.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
第二步 用git commit命令告诉git 把文件提交到仓库

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2567968-6e755fb4bc9b1cd2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
######为什么Git添加文件需要add，commit一共两步呢？因为commit可以一次提交很多文件，所以你可以多次add不同的文件，比如：
<code>
$ git add file1.txt
$ git add file2.txt file3.txt
$ git commit -m "add 3 files."
</code>

> #### git操作记录

之前已经提交了一个git学习笔记的文件,现在可以对其进行修改。
1. 通过 git status命令可以时刻掌握仓库的动态。
2. 通过git diff命令可以查看对仓库的修改记录。
3. 通过git long命令可以查看在本地仓库中的所有操作记录。
4. 如果需要吧当前文件退回到上依次修改过后的文件，可以通过<code>git reset -hard HEAD^</code>来实现，如果有三次修改记录，需要退回到两次之前的文件，则用<code>git reset -hard HEAD^^</code>命令，需要退回到几次前就加几个<code>^</code>,如果个数太多不好写，就可以写成<code>git reset -hard HEAD~n</code>.
5. git reflog命令用来记录你的每一次命令的ＩＤ号。
###### ！！！每次修改文件过后，都需要用<code>git add</code>命令对文件进行一次添加，把文件添加到暂存区，只有这样<code>git commit</code>才能记录文件的操作记录。
![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2567968-ed97aad0f8984f46.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
6. 撤销修改
-只是进行了修改还没有放到暂存区，可以通过<code>git checkout -- git学习笔记</code>可以撤销对文件的上一步修改。
-进行了修改并且放到了暂存区，那么可以通过<code>git reset HEAD file git学习笔记.md</code>把对文件的修改撤销，并且放到工作区。
7. 删除文件
-直接在文件管理器中删除。
-用<code>git rm file</code>命令进行删除。
从版本库中删除该文件，那就用命令git rm删掉，并且git commit。

> #### 添加远程库

在本地创建了一个Git仓库后，又想在GitHub创建一个Git仓库，并且让这两个仓库进行远程同步，这样，GitHub上的仓库既可以作为备份，又可以让其他人通过该仓库来协作，真是一举多得。
- 把本地库的内容推送到远程，用<code>git push</code>命令，实际上是把当前分支master推送到远程
######若是提交远程错误：则输入<code>git push -f</code>就OK了。

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2567968-e8f8821873fde525.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 把远程库克隆到本地仓库
首先要新建一个远程库，然后通过<code>git clone</code>命令进行客隆，把远成仓库，克隆到本地仓库。
<code>$ git clone git@github.com:Liyinzhe/BIubiubiu.git</code>




