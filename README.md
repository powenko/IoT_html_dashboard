# IoT_html_dashboard

**以 HTML5 建構的 IoT 資料即時儀錶板**

---

## 📘 專案簡介

`IoT_html_dashboard` 是一個使用 **純 HTML、CSS、JavaScript** 打造的輕量級 **物聯網資料可視化儀錶板（Dashboard）**。
此專案主要用於在瀏覽器上顯示感測器資料（例如溫度、濕度、氣壓、光照度等），支援從 MQTT、WebSocket 或 REST API 來源取得即時資料，並以圖表與儀錶形式呈現。

此專案強調：

* 無需伺服器端框架（例如 Node.js 或 Flask）
* 可在本地端或靜態網站主機（例如 GitHub Pages）直接運行
* 模組化架構，方便整合各種 IoT 裝置與雲端資料來源

---

## 🚀 主要功能

* **即時資料更新**：透過 WebSocket 或 MQTT 即時顯示感測器數據
* **可自訂的儀錶板元件**：支援多種圖表與指針式儀錶
* **支援多種資料來源**：REST API / MQTT / JSON 檔案
* **響應式介面設計**：支援桌機、平板、手機等多種裝置
* **輕量、易部署**：可直接以 GitHub Pages 或任何靜態伺服器運行

---

## 🧩 專案結構

```
IoT_html_dashboard/
├── index.html              # 儀錶板主頁面
├── css/
│   ├── style.css           # 主樣式檔
│   └── theme-dark.css      # 深色主題樣式
├── js/
│   ├── main.js             # 主控制邏輯
│   ├── mqtt.js             # MQTT 通訊模組（可選）
│   ├── chart.js            # Chart.js 整合模組
│   └── config.js           # 設定檔（API、主題、元件配置）
├── assets/
│   ├── icons/              # 圖示資源
│   └── fonts/              # 字型檔案
└── data/
    └── sample_data.json    # 範例感測資料
```

---

## ⚙️ 安裝與執行

### 1. 下載或複製專案

```bash
git clone https://github.com/yourusername/IoT_html_dashboard.git
cd IoT_html_dashboard
```

### 2. 啟動本地伺服器（選擇性）

若需測試 MQTT 或 WebSocket 連線，建議使用簡易 HTTP 伺服器：

```bash
# 使用 Python 內建伺服器
python3 -m http.server 8080
```

然後在瀏覽器中開啟：

```
http://localhost:8080
```

### 3. 部署至 GitHub Pages

* 前往 GitHub 專案設定 → Pages
* 選擇分支 `main` 並設為 `/ (root)`
* 儀錶板即可於 `https://yourusername.github.io/IoT_html_dashboard/` 開啟

---

## 🧠 技術細節

| 技術項目                        | 說明                          |
| --------------------------- | --------------------------- |
| **HTML5 / CSS3**            | 使用 Flexbox + Grid 佈局，支援 RWD |
| **JavaScript (ES6+)**       | 模組化撰寫，支援動態資料更新              |
| **Chart.js**                | 用於繪製折線圖、圓餅圖、指針儀表等           |
| **MQTT.js / WebSocket API** | 實現 IoT 裝置即時資料串流             |
| **JSON 設定檔**                | 儀錶板元件與主題配置集中管理              |

---

## 📊 範例畫面

可在 `index.html` 中看到：

* 左側：即時溫濕度監測卡片
* 中央：環境感測趨勢折線圖
* 右側：設備狀態指示儀錶

> 若需要連線實際感測資料，可修改 `config.js` 內的 MQTT Broker 設定或 REST API URL。

---

## 🧱 未來規劃

* [ ] 新增深色／淺色主題切換
* [ ] 增加 WebSocket 與 Grafana 整合範例
* [ ] 提供 JSON 組態自動生成器
* [ ] 支援儀錶元件拖放配置

---

## 📄 授權條款

本專案採用 [MIT License](LICENSE)。

---

## 🧑‍💻 作者

**柯博文老師（Powen Ko）**
專長：IoT 系統整合、網頁前端開發、嵌入式裝置資料視覺化
聯絡方式：`example@email.com`


