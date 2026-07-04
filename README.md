# 每日天使卡 · Daily Angel Card

一個純前端的互動式抽卡網頁。使用者每天可以從牌陣中憑直覺抽出一張天使卡，
獲得當日的訊息、關鍵字與建議行動，並且會自動把每一天抽到的卡儲存在瀏覽器中，
形成專屬於自己的每日紀錄。

## 功能

- 24 張原創天使卡／能量卡內容（卡名、關鍵字、解讀文字、今日建議）
- 扇形牌陣互動抽卡，點擊卡片觸發洗牌淡出＋翻牌動畫
- 抽卡結果頁提供「重新抽卡」按鈕，回到原始牌陣重新抽取
- 頁面最上方顯示今天的日期
- 頁面最下方常駐「每日紀錄」區塊，自動記錄每一天抽到的卡（存於瀏覽器 localStorage），
  點擊任一筆可展開查看完整解讀
- 手機優先的響應式設計、支援鍵盤操作與 `prefers-reduced-motion`

## 技術

純 HTML／CSS／JavaScript（Vanilla JS），無框架、無需建置工具、無需後端。
所有資料儲存在使用者瀏覽器的 `localStorage`（訪客模式，不跨裝置同步）。

## 如何在本機開啟

直接用瀏覽器打開 `index.html` 即可，不需要安裝任何套件或啟動伺服器。

## 檔案結構

```
.
├── index.html          # 完整的互動網頁（唯一需要的檔案）
├── docs/
│   └── 每日天使卡_PRD.docx   # 原始產品需求文件
└── README.md
```

## 上傳到 GitHub（使用 GitHub Desktop）

1. 解壓縮這個資料夾到你電腦上任一位置。
2. 打開 GitHub Desktop → `File` → `Add local repository...`，選擇這個資料夾。
3. 如果跳出「這不是 Git repository，要初始化嗎？」→ 選擇 `create a repository`。
4. 左下角輸入 commit 訊息（例如：`Initial commit: 每日天使卡互動網頁`），按下 `Commit to main`。
5. 按右上角 `Publish repository`，選擇 public 或 private，完成發布。

## 上傳到 GitHub（使用終端機 / CLI）

```bash
cd daily-angel-card
git init
git add .
git commit -m "Initial commit: 每日天使卡互動網頁"
git branch -M main
git remote add origin https://github.com/<你的帳號>/daily-angel-card.git
git push -u origin main
```

## 部署（選用）

這是純靜態網頁，可以直接部署到 Vercel、Netlify 或 GitHub Pages：

- **GitHub Pages**：repo 設定 → Pages → Source 選擇 `main` 分支 → 儲存後幾分鐘內即可透過
  `https://<帳號>.github.io/<repo名稱>/` 存取。
- **Vercel / Netlify**：直接匯入這個 GitHub repo，無需額外設定即可部署。

## 待補功能（依 PRD 規劃）

- 每日限抽一次的強制鎖定（目前為無限次重抽，同一天重複抽卡會覆蓋當天紀錄）
- 睡前感恩日記功能（PRD 第 4 章）
- 帳號系統與跨裝置同步
