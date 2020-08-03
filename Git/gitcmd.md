# 常用git命令



| 命令                                                        | 作用                                     |
| ----------------------------------------------------------- | ---------------------------------------- |
| `mkdir <file>`                                              | 在当前目录下创立名为name的文件夹         |
| `cd <file>`                                                 | 转到name目录下                           |
| `pwd`                                                       | 显示当前目录                             |
| `cat <file>`                                                | 显示file内容                             |
| `git config --global user.name "Your Name"`                 |                                          |
| `git config --global user.email “Your email”`               |                                          |
| `git init`                                                  | 把当前目录变成Git可以管理的仓库          |
| `git add <file>`                                            | 将file放入暂存区                         |
| `git commit -m "message"`                                   | 提交并添加提示信息                       |
| `git status`                                                | 查看当前状态                             |
| `git diff`                                                  | 查看不同之处                             |
| `git log`                                                   | 查看历史                                 |
| `git log --pretty=oneline`                                  | 查看历史简略显示                         |
| `git log --graph --pretty=oneline --abbrev-commit`          | 查看分支的合并情况                       |
| `git reset --hard <commit_id>`                              | 版本回退                                 |
| `git reflog`                                                | 查看历史命令                             |
| `git diff HEAD -- <file>`                                   | 查看最新修改                             |
| `git checkout -- <file>`                                    | 撤销工作区的所有更改，退回到与版本库一致 |
| `git reset HEAD <file>`                                     | 把暂存区的修改撤销掉(unstage)            |
| `ssh-keygen -t rsa -C "youremail@example.com"`              | 创建SSH                                  |
| `git remote add <origin> git@github.com:path/repo-name.git` | 建立本地与远程联系使用github             |
| `git remote add <origin> git@gitee.com:path/repo-name.git`  | 建立本地与远程联系使用gitee              |
| `git remote`                                                | 查看远程库的信息                         |
| `git remote -v`                                             | 查看远程库的信息并显示详细信息           |
| `git push -u <origin> <branch>`                             | 推送到远程(第一次推送)                   |
| `git push <origin> <branch>`                                | 推送到远程                               |
| `git clone git@github.com:path/repo-name.git`               | 克隆远程库                               |
| `git clone git@gitee.com:path/repo-name.git`                | 克隆远程库                               |
| `git pull`                                                  | 将最新的提交抓取下来                     |
| `git checkout -b <branch>`                                  | 创建并切换分支(不建议使用)               |
| `git switch -c <branch>`                                    | 创建并切换分支                           |
| `git checkout <branch>`                                     | 切换分支(不建议使用)                     |
| `git switch <branch>`                                       | 切换分支                                 |
| `git branch <branch>`                                       | 创建分支                                 |
| `git branch`                                                | 查看分支                                 |
| `git merge <branch>`                                        | 合并某分支到当前分支                     |
| `git branch -d <branch>`                                    | 删除分支                                 |
| `git merge --no-ff -m "message" <branch>`                   | 禁用Fast forward的合并某分支到当前分支   |
| `git stash`                                                 | 储藏当前工作现场                         |
| `git stash list`                                            | 查看储藏的工作现场                       |
| `git stash apply`                                           | 恢复现场但不删除                         |
| `git stash pop`                                             | 恢复现场并删除                           |
| `git cherry-pick <commit_id>`                               | 复制一个特定的提交到当前分支             |
| `git branch -D <branch>`                                    | 强制删除一个没有被合并过的分支           |
| `git rebase`                                                | 把本地未push的分叉提交历史整理成直线     |
| `git tag <name>`                                            | 在当前位置打一个新标签                   |
| `git tag <name> <commit_id>`                                | commit处打一个新标签                     |
| `git tag`                                                   | 查看标签                                 |
| `删除一个远程标签git show <tagname>`                        | 查看标签信息                             |
| `git tag -a <tagname> -m "message"`                         | 指定标签信息                             |
| `git tag -d <tagname>`                                      | 删除标签                                 |
| `git push <origin> <tagname>`                               | 送某个标签到远程                         |
| `git push <origin> --tags`                                  | 一次性推送全部尚未推送到远程的本地标签   |
| `git push origin :refs/tags/<tagname>`                      | 删除一个远程标签                         |

