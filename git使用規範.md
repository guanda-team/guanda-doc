# git 使用規範

## 🔥 Commit Message 規範

```
<type>(<scope>): <subject>

<body>

<footer>
```

## 🔥 Message Header: \<type>(\<scope>): \<subject>

- type(必要): commit 的類別
  - feat: 新增 / 修改功能
  - fix: 修補 bug
  - docs: 文件
  - style: 格式
  - refactor: 重構
  - perf: 改善效能
  - test: 增加測試
  - chore: 建構程序或輔助工具的變動
  - revert: 撤銷回覆先前的 commit
- scope(可選): commit 影響的範圍
- subject(必要): commit 的簡短描述

## 🔥 Message Body: \<body>

- 對本次 Commit 的詳細描述
- 可以分成多行
- 說明程式碼變動的項目與原因，還有與先前行為的對比

## 🔥 Message Footer: \<footer>

- 填寫任務編號

## 🔥 Commit Message 範例

```
feat: message 新增信件通知功能

feat(優惠券): 加入搜尋按鈕，調整畫面

fix: 圓餅圖圖例跑版

fix: 意見反應，信件看不到圖片問題

style: 統一換行符號 CRLF to LF

docs: 更新 README 相關資訊

docs: 修正型別註解

chore(submoudle): 變更 git url

chore: 調整單元測試環境

refactor(每日通知信件): 重構程式結構
```

## 🔥 參考資料

- [參考資料 1](https://wadehuanglearning.blogspot.com/2019/05/commit-commit-commit-why-what-commit.html)

- [參考資料 2](https://heidiliu2020.github.io/git-commit-message/)
