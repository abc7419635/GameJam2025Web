# GameJam2025 🎮

一個專為桌面環境設計的 Unity WebGL 遊戲專案，具備智能設備檢測和解析度限制功能。

## 📋 專案概述

GameJam2025 是為 Game Jam 2025 活動開發的網頁遊戲，採用 Unity WebGL 技術構建，確保在適當的設備和解析度下提供最佳遊戲體驗。

## ✨ 主要功能

### 🖥️ 智能設備檢測
- **解析度檢測** - 自動檢測用戶螢幕解析度
- **最低要求** - 要求最低解析度 1600×900
- **即時反饋** - 不符合要求時顯示友善的錯誤提示

### 🚫 設備限制
- **桌面優先** - 專為桌面電腦和大尺寸筆電設計
- **阻止低解析度設備** - 自動阻止手機、平板和小螢幕設備
- **清楚說明** - 提供明確的解決方案建議

### 🔧 調試功能
- **Console 輸出** - 提供簡潔的解析度檢測信息
- **手動檢測** - 支援 `checkResolution()` 手動檢測功能
- **重新檢測** - 頁面內建重新檢測按鈕

## 🎯 技術特色

### 📊 解析度檢測邏輯
```javascript
// 最低解析度要求：1600×900
const minWidth = 1600;
const minHeight = 900;
const isLowResolution = screenWidth < minWidth || screenHeight < minHeight;
```

### 🎨 用戶界面
- **現代化設計** - 深色主題，圓角邊框
- **響應式布局** - 適應不同螢幕尺寸
- **視覺回饋** - 清楚的圖標和顏色提示

### ⚡ 性能優化
- **Service Worker** - 支援離線快取
- **精簡 LOG** - 只輸出必要的調試信息
- **快速載入** - 優化的資源載入流程

## 📁 檔案結構

```
GameJam09/
├── BuildWeb/
│   ├── index.html          # 主要 HTML 檔案
│   ├── Build/              # Unity WebGL 建置檔案
│   │   ├── BuildWeb.data.unityweb
│   │   ├── BuildWeb.framework.js.unityweb
│   │   ├── BuildWeb.loader.js
│   │   └── BuildWeb.wasm.unityweb
│   ├── TemplateData/       # 樣式和資源檔案
│   │   ├── style.css
│   │   ├── favicon.ico
│   │   └── icons/
│   ├── ServiceWorker.js    # Service Worker 檔案
│   └── manifest.webmanifest # Web App Manifest
└── README.md               # 專案說明文件
```

## 🚀 使用方法

### 本地開發
1. 啟動本地伺服器（如 Live Server）
2. 開啟 `BuildWeb/index.html`
3. 確保螢幕解析度 ≥ 1600×900

### 部署
1. 將 `BuildWeb` 資料夾上傳到網頁伺服器
2. 確保所有檔案路徑正確
3. 訪問 `index.html` 開始遊戲

## 🔍 調試指南

### Console 輸出範例
```
📊 當前解析度: 1920 × 1080
📏 最低要求: 1600 × 900
✅ 解析度符合要求，遊戲可以運行
```

### 手動檢測
在瀏覽器 Console 中輸入：
```javascript
checkResolution()
```

### 調試模式
在網址後加上 `?debug=true` 啟用調試模式：
```
http://localhost/index.html?debug=true
```

## 📱 支援的設備

### ✅ 支援的設備
- **桌面電腦** - Windows, macOS, Linux
- **大尺寸筆電** - 15吋以上，解析度 ≥ 1600×900
- **高解析度顯示器** - Full HD, 2K, 4K

### ❌ 不支援的設備
- **手機** - 所有手機設備
- **平板** - iPad, Android 平板
- **小筆電** - 解析度 < 1600×900 的設備
- **低解析度螢幕** - 1366×768, 1280×720 等

## 🛠️ 技術規格

- **遊戲引擎** - Unity 2022.x
- **輸出格式** - WebGL
- **瀏覽器支援** - Chrome, Firefox, Safari, Edge
- **最低解析度** - 1600×900
- **建議解析度** - 1920×1080 或更高

## 📝 開發備註

### 解析度檢測邏輯
- 使用 `window.innerWidth` 和 `window.innerHeight` 檢測
- 同時檢查寬度和高度，任一不足即阻止
- 提供具體的不足項目說明

### 錯誤處理
- 友善的錯誤頁面設計
- 清楚的解決方案建議
- 重新檢測功能

### 性能考量
- 精簡的 Console 輸出
- 優化的資源載入
- Service Worker 快取支援

## 🎮 遊戲體驗

本遊戲專為桌面環境設計，需要：
- **鍵盤和滑鼠操作**
- **大螢幕顯示**
- **穩定的網路連線**

## 📞 技術支援

如遇到問題，請檢查：
1. 螢幕解析度是否 ≥ 1600×900
2. 瀏覽器是否支援 WebGL
3. 網路連線是否穩定
4. 是否啟用了 JavaScript

---

**GameJam2025** - 為桌面玩家打造的優質遊戲體驗 🚀 