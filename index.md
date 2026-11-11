# 大二行銷影展專題《暫停蔗一刻》Vibe Coding 開發歷程與 Prompt 說明檔

## 📌 專案基本資訊
- **專題名稱**：《暫停蔗一刻：關掉喧囂，在糖廠遇見平靜》
- **專案作者**：吳淳琳
- **所屬系所**：逢甲大學行銷學系（大二行銷影展專題）
- **專案核心定位**：針對 18-25 歲都市高壓族群打造之「都市情緒防空洞」
- **作業交付連結**：
  1. **GitHub Markdown (Prompt 說明檔)**：`https://github.com/[YOUR_GITHUB_USERNAME]/[REPO_NAME]/blob/main/prompts.md`
  2. **InfinityFree 部署網站**：`http://[YOUR_INFINITYFREE_DOMAIN].infinityfreeapp.com/`
  3. **Vercel 部署網站**：`https://[YOUR_VERCEL_PROJECT].vercel.app/`

---

## 🤖 Vibe Coding 指令紀錄 (Prompt Log)

本專案採用 Vibe Coding 模式，將行銷企劃內容、視覺草圖與色卡規格，透過階段式 Prompt 指令轉換為符合網頁開發規範之專題網站。以下為核心提示詞紀錄：

### 階段一：企劃書轉網頁架構 (Document Parsing)
```text
「我是大二學生，影展專題主題是『暫停蔗一刻』。這是我給你的行銷影展企劃書 PDF。請幫我分析並整理出：帝國製糖廠簡介、景點特色、周邊景點介紹、現況與未來趨勢、SWOT 分析（請用 2x2 表格陣列呈現）、STP 分析、廣告目標與精神，以及影片展示區塊。」
```

### 階段二：手繪草圖轉化與 `nature's touch` 色調設定 (Layout & Color Palette)
```text
「1. 請幫我將網站頂部調整為手繪草圖的版型：頂部導覽列按鈕右對齊；Hero 區塊左邊為靠左置中的標題『暫停蔗一刻』、子標題與對話框線標籤『城市再忙，別忘了充電』；右邊放置帝國製糖廠照片。
2. 請完全套用 `nature's touch` 色卡色彩：奶茶色 #e2dacc、沙褐 #c8baa6、橄欖綠 #8a9e78、暖大地棕 #a68b70、深木褐 #4a3f35、鼠尾草綠 #c0d0bd。
3. 作者標記為吳淳琳個人作業。」
```

### 階段三：藝文雜誌風革新 (Editorial Design & Matrix Upgrade)
```text
「網站不夠創意有藝術感，太中規中矩了！請重新改革格式，保留 `nature's touch` 色系，但打造出藝文雜誌風：
- 加上大型章節藝術大字編號（01 / 02 / 03）。
- SWOT 與 STP 改用錯落的大地色系藝術卡片。
- 加入膠片感相框、標籤與巨型詩意 Slogan 宣言 Banner。」
```

### 階段四：影音媒體嵌入與 CSS 模組化 (Media Embedding & CSS Refactoring)
```text
「請將 YouTube 廣告影片 https://youtu.be/RGO5_J7mAYs 嵌入至網頁 Section 05，並確保影片在手機與電腦端都能自動適應比例（RWD Aspect Ratio）。同時將 CSS 獨立切割至 css/style.css。」
```

---

## 🛠️ 網頁技術規範與專案結構

1. **目錄結構**：
   ```text
   📁 專案根目錄/
   ├── 📄 index.html          (主網頁檔案)
   ├── 📄 prompts.md          (Vibe Coding 說明文件)
   ├── 📁 css/
   │   └── 📄 style.css       (外部獨立樣式表)
   └── 📁 images/             (靜態圖片資源庫)
   ```

2. **前端技術與 RWD 規範**：
   - **語意化 HTML5**：全面使用 `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>` 標籤。
   - **SEO 最佳化**：配置元資料 (Meta Tags) 與 Open Graph (OG) 社群卡片標籤。
   - **網格與自適應佈局**：採用 CSS Grid 及 Flexbox，桌機端為 `1fr 310px` 雙欄佈局，行動端（`max-width: 960px`）自動轉換為單欄流體順序。
   - **色彩體系**：使用 CSS 變數統一管理全站自然大地色系 (`#e2dacc`, `#c8baa6`, `#8a9e78`, `#a68b70`, `#4a3f35`, `#c0d0bd`)。