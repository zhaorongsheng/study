#### git保存密码配置
1. 方法一
git config --global credential.helper store
2. 方法二
cd ~
touch .git-credentials
vim .git-credentials
https://{username}:{password}@github.com

##git操作总结

[简单操作介绍](http://www.ruanyifeng.com/blog/2014/06/git_remote.html)


1. github与fork的代码同步方法

- 方法一：
	- 先把B clone到本地
		git clone B_REPOSITORY_URL
	- 再cd到本地B的目录，把A作为一个remote加到本地的B中（一般命名为upstream）
		git remote add upstream A_REPOSITORY_URL
	- pull另一个A的remote（upstream）的相应分支（比如master）就可以
		git pull upstream master
	- 最后push回github的B_REPOSITORY
		git push origin master

- 方法二（其实一样）：
	* git remote -v
		确定是否建立主repo的远程源(只有orign)
	* git remote add upstream URL(.git)
		添加主repo的远程源(orign和upstream)
	* git fetch upstream
		fetch远程源
	* git merge upstream/master
		与主repo合并
	* git push