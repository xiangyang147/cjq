一个新的项目使用git
git add . //添加全部文档

git commit -m "提交readme文档" //提交文档

git branch -M main //创建main分支并切换到main

git branch -a //查看分支

git checkout //查看分支下文档

git remote add origin https://github.com/xiangyang147/cjq.git //添加一个远程仓库地址连接

git push -u origin main//上传到远程仓库main分支 

其他人进入github仓库点击fork将代码复制到自己仓库

提交记录到仓库

git add . //添加全部文档

git commit -m "提交readme文档" //提交文档

git branch 0.1  //创建0.1分支

git push -u origin 0.1//上传到远程仓库main分支

git checkout 0.1 //切换分支到0.1

git clone https://github.com/xiangyang147/cjq.git . //克隆仓库文件到本地当前文件夹

git remote -v //查看自己仓库连接权限

git  remote add upstream https://github.com/xiangyang147/cjq.git //添加上游库的代码连接

git fetch upstream //更新一下本地版本(与仓库版本不一致)

git merge upstream/main //把远程upstream代码main分支merge最新的内容到目前本地分支

git push 



