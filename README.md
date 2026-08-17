# punch-bot-ui

個人打卡／班表機器人的 **Telegram Mini App 前端**，只有一支靜態網頁。

- `schedule.html` — 劃休假表的月曆介面。由 Telegram bot 以 WebApp 按鈕開啟，
  班表資料透過網址 fragment（`#d=<base64>`）在**用戶端**帶入，選完用 `tg.sendData()` 回傳給 bot。

## 為什麼這裡沒有後端

這頁**不連任何伺服器**，也沒有任何 API 金鑰。它不知道公司系統在哪、不儲存也不上傳任何東西：

- 資料放在網址 fragment，**瀏覽器不會把 fragment 送給伺服器**，所以班表內容不會出現在 GitHub Pages 的存取紀錄裡。
- 直接開這個網址只會看到「缺少班表資料」。
- 真正的登入與寫入全部發生在使用者自己電腦上的 bot（私有 repo）。

## 授權

MIT
