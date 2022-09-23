环境：本地分支master，dev，将dev分支合并到master分支
    //1. 切换到master分支
    git checkout master
    
    //2. 将dev分支合并到master分支。如果没有冲突，此时完成合并，如果有冲突，继续下面流程
    git rebase dev
    
    //3. 根据冲突文件，解决冲突

    //4. 继续rebase操作(此时会提示，如果有解决完冲突，需要git add .)
    git rebase --continue
    git add .
    //5. 再次继续rebase操作
    git rebase --continue
    
    //6. 放弃rebase操作
    git rebase --abort

环境：本地分支dev，远程分支origin/dev，拉取并合并远程分支origin/dev
    // 1. 切换到dev分支
    git checkout dev

    //2. 拉取远程分支origin/dev。如果没有冲突，此时完成合并，如果有冲突，继续下面流程
    git pull --rebase
    
    //3. 根据冲突文件，解决冲突

    //4. 继续rebase操作(此时会提示，如果有解决完冲突，需要git add .)
    git rebase --continue
    git add .
    //5. 再次继续rebase操作
    git rebase --continue
    
    //6. 放弃rebase操作
    git rebase --abort
