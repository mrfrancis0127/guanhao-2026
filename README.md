# 陳冠豪競選網站

彰化縣花壇鄉民代表第一選區候選人 陳冠豪　競選網站原型。

**Slogan**：年輕行動　翻轉花壇

---

## 📁 檔案結構

```
chen-guanhao-site/
├─ index.html              ← 主頁面
├─ README.md               ← 本說明
├─ .nojekyll               ← GitHub Pages 用
└─ images/
   ├─ portrait.webp        ← 候選人形象照
   ├─ gallery-1-school.webp     ← 母校花壇國中
   ├─ gallery-2-canvas.webp     ← 掃街拜票
   ├─ gallery-3-temple.webp     ← 虎山岩拜廟
   ├─ gallery-4-children.webp   ← 兒童節公益
   ├─ og-image.jpg              ← 社群分享預覽
   ├─ favicon.png
   ├─ favicon-32.png
   ├─ favicon-96.png
   └─ favicon-180.png
```

---

## 🎨 設計風格定位

這是三位候選人裡**第三種完全不同的調性**：

| 特性 | 泰祥版 | 尚裕版 | 冠豪版 |
|---|---|---|---|
| 主軸 | 在地・溫暖・親民 | 克制・專業・新世代 | **動感・銳利・有衝勁** |
| 主色 | 青色 + 奶油 | 青色 + 深石墨 | 青色 + **珊瑚紅**（撞色） |
| 字體 | 圓潤序列 | 嚴謹編輯 | **粗體與斜體混用** |
| 訴求 | 在地之子 | 新一代鄉政 | **年輕翻轉** |
| 視覺特徵 | 旋轉光環 | 幾何網格 | **斜線、撞色、大數字** |

**冠豪版專屬視覺特徵**：
- 珊瑚紅 `#E5564B` 作為「翻轉」能量色，跟青色形成強烈對比
- 全站使用 **8° 偏斜（skew）** 元素：CTA 按鈕、徽章、編號
- Hero 背景有對角線條紋
- 政見卡片用粗黑邊框（2px）的網格排列，像報紙版面
- 「翻轉花壇」斜體 + 旋轉 -1.5°，視覺上真的「翻轉」

---

## 🚀 部署

### Cloudflare Pages（推薦，無點數限制）
1. 註冊 cloudflare.com（免費）
2. Workers & Pages → Create → Upload assets
3. 拖入解壓後的整個資料夾
4. 取得網址 `xxx.pages.dev`

### GitHub Pages
1. 新建 public repo
2. 上傳所有檔案（**注意 images 資料夾要完整上傳**）
3. Settings → Pages → Source: Deploy from a branch (main, /)
4. 取得網址 `username.github.io/repo-name/`

### Vercel
拖 ZIP 到 vercel.com 也可以。

---

## ✏️ 上線前必改清單

### 候選人本人審閱
- [ ] **理念** section：故事素材取自 PDF 自傳，但語氣需冠豪本人潤稿
- [ ] **8 大行動方針**：方向 OK，但具體項目需與冠豪確認
- [ ] **登記號次**：Hero 紅圈內留空，抽到號次後在 `index.html` 搜尋 `class="hero-badge-num"` 填入

### 必確認的隱私資訊
- [ ] **服務專線**：目前顯示 `0952-970-01X`（PDF 上的號碼缺一碼），確認完整號碼
- [ ] **Email**：`aux5088@gmail.com` 是冠豪個人 Gmail，建議申辦競選專用 email
- [ ] **服務處地址**：目前留空，待設置後填入（不要用戶籍地）
- [ ] **LINE 官方帳號**：待申辦後替換
- [ ] **Facebook 粉專連結**：待提供

### 法律
- 移除頂部黑色「PROTOTYPE」橫幅（搜尋 `class="demo-banner"` 刪除整個 div）
- 確認照片使用權（特別是與第三人合影的照片）
- 競選經費勸募須先依《政治獻金法》備案

---

## 後續

- 拿到正式 LINE@、競選服務處地址後告訴 Claude，全部更新
- 想加新政見、新照片、新影片，隨時可調整
- 若需替換成其他主色（例如改用更深紅、改用紫等），可以一行 CSS 變數變更全站色系
