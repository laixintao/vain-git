# vain-git
虚荣的git，填满 Github 日历。

## 使用方法
1. 修改这个脚本中 `username` 为你的 Github 用户名;
2. 将脚本复制到你的 `$PATH` 路径下，然后为其增加执行权限即可，这个脚本没有任何三方依赖，只要有 Python3 就可以运行.

使用 `fgc` 来替代 `git commit`，`fgc` 会自动添加上一个你在 Github 上没有提交记录的日期。 `fgc -m "this is a commit"` 等效于 `git commit --date=1594729017 -m "this is a commit"`.

## 原理
获得过去1年 Github 的 commit 数据。找到第一个没有提交记录的格子，将这个格子的日期作为 `--date=?` 的参数然后启动 `git commit` 进程来完成提交。
