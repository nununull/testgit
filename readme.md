# git常用命令

一、git 常用命令：
1、git status		查看当前分支状态

2、新建一个项目
先到服务器新增一个项目名称

```git
git init

git remote add origin ssh://git@git.dev.dianxiaomi.com:36022/third-party/sfbsp-ws-sdk.git

git add .

git commit

git push -u origin master

```


3、git clone 克隆一个项目到本地


```
git clone ssh://git@git.dev.dianxiaomi.com:36022/third-party/sfbsp-ws-sdk.git
```

4、	新建分支、fix--

```
git branch wip-product-wish
```


删除分支
方法一：
git branch -d		删除本地分支	
git push --delete origin wip-wish-product 删除线上分支



5、git add .		新增文件，加入版本控制

6、git commit		提交代码

7、git pull		同步服务器数据

8、git push		提交本地数据到服务器
​		
9、git rebase/merge	合并代码

10、git checkout	切换分支

-------------------------------------------------------------------

二、项目中使用
1、新建分支、开发、分支提交 
git branch branchName
git checkout branchName
开发
测试
git commit 
git pull
git push

2、切换主干，更新主干数据
git checkout master
git pull

3、切换分支，把主干代码合并到分支
git checkout branchName
git pull
git rebase master
可能有冲突,有冲突，先解决
git pull
git push

4、切换主干，主干合并分支的代码，上线


```git
git checkout master

git rebase branchName

git pull

git push

```