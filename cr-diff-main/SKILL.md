---
name: cr-diff-main
description: 只有当用户明确说 cr-diff-main 时才使用。
---

# 对比 Main 做 CR

用于 review 当前分支相对最新 `main` 的改动。

## 流程

1. 确保当前分支干净：
   - 所有修改都必须已经 commit。
   - 如果当前分支不干净，先停止并提醒用户。

2. 确保 `main` 是最新的，并且和远程一致：
   - 如果不一致，先把 `main` 和远端 `origin/main` 保持一致。
   - 对比时优先使用远端 `origin/main`。

3. 对比当前分支和最新 `main`，然后做 CR。


## CR问题列表输出格式


## 注意

- 避免：自动部署、push、merge、rebase、reset。
- 避免给出非本批次修改引入的问题，避免给出历史问题。
- 确保影响已有功能的问题都被识别出来。
