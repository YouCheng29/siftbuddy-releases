# SiftBuddy 下載

SiftBuddy 是 macOS 選單列的 GitHub 通知 app。這個 repo 只放安裝檔與更新清單，程式碼不在這裡。

> **只從這個頁面的 [Releases](https://github.com/YouCheng29/siftbuddy-releases/releases) 下載。別人用 Slack、Email 或雲端硬碟轉傳給你的檔案，不要開。**
> 這個 app 沒有經過 Apple 公證，macOS 不會替你檢查它有沒有被動過手腳，所以下載後請核對校驗碼。

## 需求

- macOS 14（Sonoma）或更新版本
- 已安裝 GitHub CLI（`gh`）並登入。第一次開啟時的歡迎視窗會幫你檢查，也會給你要貼的指令

## 安裝

1. 到 [最新版](https://github.com/YouCheng29/siftbuddy-releases/releases/latest) 下載 `SiftBuddy-<版本>.zip`
2. 核對校驗碼（見下）。不一致就不要解壓縮、不要打開，把檔案刪掉
3. 雙擊 zip 解壓縮，得到 `SiftBuddy.app`
4. 已經裝了舊版：點選單列的 SiftBuddy 圖示，從齒輪選單選「結束 SiftBuddy」
5. 把 `SiftBuddy.app` 拖進「應用程式」資料夾。已經有舊版時選「取代」

### 核對校驗碼

校驗碼是從檔案內容算出來的一串英數字，檔案只要差一個位元，算出來就完全不同。下載頁的說明裡有這一版的校驗碼。在終端機算出你下載的檔案的校驗碼（把 `<版本>` 換成實際版本）：

```bash
shasum -a 256 ~/Downloads/SiftBuddy-<版本>.zip
```

輸出的第一欄（64 個英數字）要和下載頁上的校驗碼完全相同。有任何一個字不同，就不要開。

## 第一次開啟

這個 app 沒有經過 Apple 公證，第一次雙擊會被 macOS 擋下。依你的 macOS 版本擇一。

macOS 14：

1. 在「應用程式」裡對 `SiftBuddy` 按右鍵（或 Control＋點擊）
2. 選「打開」
3. 跳出警告視窗後，再按一次「打開」

macOS 15 以上：

1. 在「應用程式」裡雙擊 `SiftBuddy`，被擋下時按「完成」
2. 打開「系統設定 → 隱私權與安全性」，捲到最下面的「安全性」
3. 找到「已阻擋 SiftBuddy」，按「仍要打開」
4. 輸入密碼或用 Touch ID 確認，再按一次「打開」

只有第一次要這樣做。不要用終端機指令移除 macOS 的隔離標記，那會讓 macOS 完全不再檢查這個 app。

## 更新

有新版時 app 會跳出視窗。按「安裝更新項目」，下載完再按「安裝並重新啟動」，就會換成新版並重新開啟。app 會先確認新版有正確的簽章，簽章不對就不安裝。也可以到「設定 → 一般 → 檢查更新…」自己檢查。

用 0.2.0 或更早版本的人，app 還不會自己更新：照上面的「安裝」做一次，取代舊的 app。之後就由 app 自己提醒。
