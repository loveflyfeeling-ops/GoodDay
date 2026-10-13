# 擇日通書 — 上架說明

這個資料夾就是完整網站，不需要伺服器程式，任何靜態網站空間都能放。

## 檔案
- `index.html` 主程式
- `lib/` 曆法庫 lunar-javascript、繁體轉換 opencc-js（已內建，不依賴外部 CDN）
- `icons/`、`manifest.webmanifest`、`sw.js` 手機「加入主畫面」與離線使用
- `robots.txt` 允許搜尋引擎收錄

## 方法一：Netlify Drop（最快，免註冊也可試用）
1. 打開 https://app.netlify.com/drop
2. 把整個 `zeri-site` 資料夾拖進網頁
3. 幾秒後拿到網址（例如 xxx.netlify.app），註冊後可改名或綁自己的網域

## 方法二：GitHub Pages（免費、穩定）
1. 在 GitHub 新增一個 repository（例如 zeri）
2. 上傳本資料夾內所有檔案（index.html 要在最外層）
3. Settings → Pages → Branch 選 main、資料夾選 / (root) → Save
4. 約一分鐘後網址為 https://你的帳號.github.io/zeri/

## 方法三：Cloudflare Pages
Workers & Pages → Create → Pages → Upload assets，上傳此資料夾即可。

## 綁定自己的網域
在上述平台的 Domain 設定加入網域，再到網域商把 CNAME 指向平台給的網址。

## 更新
改好 index.html 後重新上傳覆蓋即可；如果有改檔案，把 `sw.js` 第一行的 `zeri-v2` 改成新版本號（如 `zeri-v3`），使用者才會拿到新版。

## 授權
lunar-javascript 與 opencc-js 皆為 MIT 授權，授權文字放在 `lib/`。
