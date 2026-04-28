# google-cybersecurity-notes

這個 repository 現在是舊 GitHub Pages 網址的轉址 stub：

- 舊站網址：`https://gyozalab.github.io/google-cybersecurity-notes/`
- 新站網址：`https://gyozalab.github.io/gyoza-course-notes/`

## 品牌升級說明

這個專案一開始是「煎餃的 Google Cybersecurity 學習筆記」，原本聚焦在單一學程。

後來站台逐步擴充成更完整的課程筆記平台，專案定位也跟著升級：

- 從 `google-cybersecurity-notes`
- 升級為 `gyoza-course-notes`

新的名稱更符合目前的內容範圍：它不再只是 Google Cybersecurity 筆記，而是 gyozalab 旗下的多學程學習筆記站。

## 技術說明

GitHub repository 改名後，舊的 GitHub Pages 路徑不會自動保留。

這代表如果這個 repository 直接消失，原本的 Pages 網址就會失效。為了讓舊連結仍然可用，這個 repo 被刻意保留成一個輕量的轉址層。

它的用途很單純：

- 保留過去分享出去的連結
- 接住舊的 GitHub Pages 路徑
- 把訪客導向 `gyoza-course-notes` 的正確位置

## 這個 repo 裡有什麼

```text
.
|-- index.html
|-- 404.html
`-- README.md
```

- `index.html`：把舊首頁轉到新版的 cybersecurity 入口頁
- `404.html`：接住舊子路徑，重新映射到新站
- `README.md`：說明這個 repository 為什麼還存在

## 轉址邏輯

這組轉址頁會盡量保留舊連結的可用性：

1. 移除舊 base path `/google-cybersecurity-notes/`
2. 正規化舊的 `.html` 後綴
3. 把舊的 cybersecurity 筆記路徑導向 `/gyoza-course-notes/cybersecurity/...`
4. 其他情況則回退到新站根目錄

## 維護原則

這個 repo 應該保持精簡、穩定。

- 不再放新的課程內容
- 不把它當成主專案 repo 使用
- 只有在目標網址或轉址規則變動時才更新

如果未來新站結構再次調整，請同步更新 `index.html` 與 `404.html` 內的 `newBase` 常數。
