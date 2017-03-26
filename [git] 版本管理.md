#Git 版本管理

###远程仓库
生成密钥：ssh-keygen -t rsa -C "zhulinjie_cool@126.com"  
克隆远程仓库：git clone git@114.112.154.146:test/demo.git  
克隆github上的远程仓库(master分支)：git clone git@github.com:jiezeal/StudyNote.git  
克隆github上的远程仓库(dev分支)：git clone -b dev git@10.100.1.76:php/teachmgt.git  

###分支管理
git remote remove origin
git remote add origin git@git.4000669696.com:weiyuyan/groups.git
将本地指定分支推送到远程服务器的某个分支：git push origin zhulinjie:zhulinjie 【 第一个zhulinjie表示本地分支名，第二个zhulinjie表示远程分支名 】  
创建分支：git branch zhulinjie  
切换分支：git checkout zhulinjie  
创建并切换分支：git checkout -b zhulinjie  
查看分支：git branch  
合并指定分支到当前分支：git merge newbranch  
删除分支：git branch -d zhulinjie  
强制删除分支：git branch -
将某个远程主机的更新，全部取回本地：git fetch  
取回origin主机的master分支: git fetch origin master  
查看远程分支：git branch -r  
查看所有分支：git branch -a  
在origin/master的基础上，创建一个新分支：git checkout -b newBrach origin/master  
此外，也可以使用git merge命令或者git rebase命令，在本地分支上合并远程分支：
git merge origin/master  或者  git rebase origin/master  
删除远程分支：git push origin --delete 分支名  
查看远程仓库地址：git remote -v  
拉取远程分支的更新到本地：git pull origin 远程分支名:本地分支名  

场景：
正式服务器课时统计出了BUG

解决步骤：
```
cd teaching
git fetch origin Ver_1.0			// Ver_1.0 当前正式服务器版本
git checkout Ver_1.0
...									// 解决BUG
git add .
git commit -m '修复课时统计BUG'		
git push origin Ver_1.0:Ver_1.0.1	
```








