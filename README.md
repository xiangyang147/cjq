一个新的项目使用git
git add . //添加全部文档

git commit -m "提交readme文档" //提交文档

git branch -M main //创建main分支并切换到main

git branch -b my-feature //将main分支中的代码拷贝到my-reature中一份

git branch -a //查看分支

git checkout //查看分支下文档

git remote add origin https://github.com/xiangyang147/cjq.git //添加一个远程仓库地址连接

git push -u origin main//上传到远程仓库main分支 

其他人进入github仓库点击fork将代码复制到自己仓库

提交记录到仓库

git add . //添加全部想修改的文档

git commit -m "提交readme文档" //提交给git本地的文档

git branch 0.1  //创建0.1分支

git push -u origin 0.1//git上传文件到远程仓库github的main分支中

git checkout 0.1 //切换分支到0.1

git clone https://github.com/xiangyang147/cjq.git . //克隆仓库文件到本地当前文件夹

git remote -v //查看自己仓库连接权限

git  remote add upstream https://github.com/xiangyang147/cjq.git //添加上游库的代码权限

git fetch upstream //更新一下本地版本(与仓库版本不一致)

git merge upstream/main //把远程upstream代码main分支merge最新的内容到目前本地分支

git push 

git diff //本地做的改变,在下一步操作之前输入命令查看

git checkout main //切换分支到main

git pull origin master //将远端的main更新的代码同步到

git和本地disk中


规范化的工作流程
1.git clone // 到本地

2.git checkout -b xxx 切换至新分支xxx

（相当于复制了remote的仓库到本地的xxx分支上

3.修改或者添加本地代码（部署在硬盘的源文件上）

4.git diff 查看自己对代码做出的改变

5.git add xxx上传更新后的代码至暂存区

6.git commit xxx可以将暂存区里更新后的代码更新到本地git

7.git push origin xxx 将本地的xxx git分支上传至github上的git
-----------------------------------------------------------

（如果在写自己的代码过程中发现远端GitHub上代码出现改变）
1.git checkout main 切换回main分支

2.git pull origin master(main) 将远端修改过的代码再更新到本地

3.git checkout xxx 回到xxx分支

4.git rebase main 我在xxx分支上，先把main移过来，然后根据我的commit来修改成新的内容
（中途可能会出现，rebase conflict -----》手动选择保留哪段代码）

5.git push -f origin xxx 把rebase后并且更新过的代码再push到远端github上
（-f ---》强行）

6.原项目主人采用pull request 中的 squash and merge 合并所有不同的commit
----------------------------------------------------------------------------------------------
远端完成更新后
1.git branch -d xxx 删除本地的git分支
2.git pull origin master 再把远端的最新代码拉至本地


主分支main合并次分支feature时使用，ferture开发测试完成使用 merge
次分支feature需要主分支main的更新内容时，使用    rebase会保留主分支main的更新记录


