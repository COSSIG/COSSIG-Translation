# 使用 GitHub Web

## 前置条件

1. 一个现代浏览器，如 Firefox、Chrome、Edge、Safari 等。
2. 稳定的网络连接。
3. 一个 GitHub 账号（[申请](https://github.com/signup)）。

## 流程简介

1. 复刻仓库 或 同步上游
2. 

## 复刻仓库

注意：此步骤仅为**初次翻译**而准备。

进入 TranslateProject 的仓库主页：https://github.com/COSSIG/TranslateProject，点击右上角的 “Fork” 按钮将仓库复刻到自己名下。

![](../assets/images/fork-web.jpg)

在跳转的新页面中，点击下方的 “Create fork” 按钮，确认复刻。

![](../assets/images/create-fork-web.jpg)

成功后，你就有一个自己的 TranslateProject 仓库了，并且它此时与上游仓库（COSSIG/TranslateProject）完全一致。

![](../assets/images/created-fork-web.jpg)

在这个仓库，你可以进行任何操作。在遇到棘手的问题时，你甚至可以删除掉自己的仓库，重新复刻（如果你有任何需要保留的修改，请另行备份）。

## 同步上游

注意：此步骤仅为**再次翻译**而准备。

进入 TranslateProject 的仓库主页：https://github.com/COSSIG/TranslateProject，观察文件列表上方的小提示。如果它显示 “This branch is up to date with COSSIG/TranslateProject:main.”，说明仓库当前已经与上游一致，无需同步。

然而，如果它显示 “This branch is X commits behind COSSIG:main”，则说明仓库当前未与上游保持同步，我们需要手动执行同步操作。

点击小提示右边的 “Sync fork” 按钮，页面弹出一个小框，再次提醒我们 “This branch is out-of-date”。于是，我们点击下方的 “Update branch” 按钮。

![](../assets/images/sync-fork-web.jpg)

等待几秒，页面刷新，小提示内容变为 “This branch is up to date with COSSIG/TranslateProject:main.”，同步成功。
