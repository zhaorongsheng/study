#### git保存密码配置
1. 方法一
git config --global credential.helper store
2. 方法二
cd ~
touch .git-credentials
vim .git-credentials
https://{username}:{password}@github.com

