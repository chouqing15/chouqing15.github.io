# git分支规范

- 主分支 `main`
- 测试分支 `test` 不与任何分支合并
- 开发分支 `dev` 所有的功能分支合并到dev
- 功能分支 `feature/需求_时间` 所有的功能分支从`dev`迁出， 分支名尽量不用中文
- bug分支 `hotfix/xxx` bug分支统一从`main`分支迁出

## 代码提交规范

- 功能代码提交 `feat: 开发功能描述`
- bug代码提交 `fix: bug修复描述`

> 合并目标分支前须将目标分支对当前分支进行合并一次，解决冲突

## 创建分支流程

- 需求分支创建： 从`develop`分支拉需求分支，再从需求分支拉各自的开发分支 。开发完成合并， 需求分支 => `develop`分支 => `main`分支
- bug分支创建：从`main`分支创建出新分支，开发完毕之后合并到main和develop分支


## 合并分支和部署环境流程

dev环境： 开发统一合并到需求分支再合并到`develop`分支， 从`develop`中打包部署到开发环境

test环境： 将开发好的dev分支代码合并到test分支并进行部署，测试分支的代码只进不出任何分支不与`test`分支进行合并

prod环境： 将测试好的develop分支的代码合并到main分支并进行部署， develop 分支的代码应始终和main分支保持同步


**merge到目标分支前需先将目标分支merge一次自己的分支**

**merge到目标分支前需先将目标分支merge一次自己的分支**

**merge到目标分支前需先将目标分支merge一次自己的分支**