# google-cybersecurity-notes (stub repo)

> ⚠️ 這個 repo 沒有實際內容，只用來維持舊網址 `https://gyozalab.github.io/google-cybersecurity-notes/` 可達。

## 為什麼有這個 repo？

原本「煎餃的 Google Cybersecurity 學習筆記」站台升級為多學程版時，repo 從 `google-cybersecurity-notes` 改名為 `gyoza-course-notes`。

GitHub repo 改名 → URL 跟著變 → **舊 GitHub Pages URL 會 404**。為了讓之前分享過的連結（社群、書籤、訊息）仍可達，把 `google-cybersecurity-notes` 這個名字重新建一個 stub repo，內容只有兩個 HTML 檔做 client-side redirect。

## 結構

```
.
├── index.html      # 首頁 redirect → cybersecurity/MOC
├── 404.html        # 任何子路徑都被 GitHub Pages 路由到這（GitHub Pages 對 user/org 站特性）
└── README.md       # 你正在看
```

## 跳轉邏輯

`index.html` / `404.html` 內的 JS：
1. 抓 `window.location.pathname`
2. 移除 base path `/google-cybersecurity-notes/`
3. 判斷舊站結構：
   - 空路徑 → 新站 `/cybersecurity/MOC`
   - `C{N}_` 開頭 → 新站 `/cybersecurity/{path}`
   - 其他 → 新站根目錄
4. `meta refresh` 3 秒後跳；JS 倒數結束後 `window.location.replace`

## 部署

1. 在 GitHub 建立 repo `gyozalab/google-cybersecurity-notes`
2. push 本資料夾內容到 main
3. Settings → Pages → Source 選「Deploy from a branch / main / root」（不是 GitHub Actions，因為沒有 build）
4. 訪問 `https://gyozalab.github.io/google-cybersecurity-notes/` 確認 redirect 正常

## 維護

平時不需要動。除非：
- 改新站 URL → 改 `index.html` / `404.html` 裡的 `newBase` 變數
- 確認舊 URL 不再有人用了 → 可以關掉這個 repo（建議至少維持 1 年）
