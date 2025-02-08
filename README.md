# Vue 專案 README

## 專案簡介

這是一個 Vue.js 專案，使用 Vue 3 + Vite 進行開發與構建。

## 環境需求

- Node.js 版本: 16.x 以上
- npm 或 yarn

## 安裝依賴

```sh
npm install
# 或者使用 yarn
yarn install
```

## 啟動開發伺服器

```sh
npm run dev
# 或者使用 yarn
yarn dev
```

## 建置專案

```sh
npm run build
# 或者使用 yarn
yarn build
```

## 資料夾結構

專案的主要目錄結構如下：

```
├── src/               # 主要程式碼目錄
│   ├── assets/        # 靜態資源 (圖片、CSS 等)
│   ├── components/    # 可重複使用的 Vue 元件
│   ├── pages/         # 頁面級組件
│   ├── router/        # Vue Router 配置
│   ├── store/         # 狀態管理 (如果使用 Vuex 或 Pinia)
│   ├── services/      # API 請求相關封裝
│   ├── utils/         # 公用工具函式
│   ├── App.vue        # 主要 Vue 入口組件
│   ├── main.js        # 入口文件
├── public/            # 靜態文件 (favicon, index.html 等)
├── .eslintrc.js       # ESLint 設定檔
├── .prettierrc        # Prettier 設定檔
├── package.json       # 專案依賴與腳本
└── README.md          # 專案說明文件
```

- **`components/`**：存放可重用的 Vue 元件。
- **`pages/`**：存放頁面級的組件，每個頁面為單獨的 `.vue` 文件。
- **`router/`**：用於管理 Vue Router 配置。
- **`store/`**：如果使用 Vuex 或 Pinia 來管理應用狀態，則在此目錄中存放。
- **`services/`**：封裝 API 請求，讓元件不直接調用 API。
- **`utils/`**：放置公用函式，如日期格式化、數據轉換等。

## 程式碼風格 (Coding Style)

### 1. 格式化工具

專案使用 [ESLint](https://eslint.org/) 和 [Prettier](https://prettier.io/) 來維持程式碼風格。

- **ESLint**: 負責程式碼語法檢查
- **Prettier**: 用於程式碼格式化

#### 安裝擴充功能：

如果你使用 VS Code，建議安裝以下擴充功能來確保格式統一：

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

### 2. 代碼風格指南

- 使用 **Composition API** 撰寫 Vue Component。
- 組件名稱採用 `PascalCase`，例如 `MyComponent.vue`。
- 變數名稱使用 `camelCase`，例如：
  ```js
  const myVariable = 'Hello';
  ```
- 常數使用 `UPPER_CASE` 命名，例如：
  ```js
  const API_URL = 'https://api.example.com';
  ```
- 每個 Vue 組件內部的部分應按照 **順序** 擺放：
  1. `script` (setup 相關邏輯)
  2. `template`
  3. `style`
- 儘量避免在 `setup` 內直接操作 DOM，應使用 `ref` 或 `computed`。
- CSS 樣式統一使用 **SCSS**，並啟用 **Scoped CSS**。
- 使用 `async/await` 進行異步操作，避免過度使用 Promise chaining。
- API 呼叫應該封裝在 `services` 目錄內，不應直接在組件中發送請求。

### 3. Git Commit 規範

```sh
type: message
```

#### 常見 `type` 類型：

- `feat`：新增功能
- `fix`：修復錯誤
- `docs`：修改文件
- `style`：調整格式（不影響程式邏輯）
- `refactor`：程式碼重構
- `test`：新增或修改測試
- `chore`：其他雜項，如更新依賴

#### 範例：

```sh
git commit -m "feat: add login feature"
```

## 結語

請確保所有 PR 都通過 ESLint 檢查並符合程式碼風格指南，感謝你的貢獻！

