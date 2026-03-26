# OpenClaw 安裝指南

> 作者：lyscnf23  
> 環境：VirtualBox - Ubuntu
> API：Google

---

## 1. 安裝 Node.js

### 安裝 curl

```bash
sudo apt install -y curl
```

### 安裝 Node.js

```bash
curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt install -y nodejs
```

### 確認安裝

```bash
node --version
```

---

## 2. OpenClaw 安裝與設定

### 前置準備

準備好 API Key（範例使用 Google 的）

### 安裝 OpenClaw

```bash
npx openclaw onboard
```

### 設置步驟

1. 出現警告畫面後，右鍵選擇 **Yes**
2. **Setup mode** 選 `QuickStart`
3. **Model/auth provider** 選 `Google`（示範）
4. **Default model** 選 `google/gemini-2.5-flash-lite`（推薦）
5. **Select channel (QuickStart)** 選 `WhatsApp`（示範）
   - **Link WhatsApp now (QR)** 選 `Yes`
   - 在手機上安裝 WhatsApp
   - 前往「設定」→「已連結裝置」→「連結裝置」→ 掃描 QR Code
   - **WhatsApp phone setup** 選 `This is my personal phone number`
   - 在 **Your personal WhatsApp number** 填入 WhatsApp 註冊手機號碼（國碼 + 手機號）
6. **Search provider** 選 `DuckDuckGo Search (experimental)`（示範）
7. **Install missing skill dependencies** 按空白鍵選擇以下項目（失敗沒關係，之後可補裝）：
   - `github`
   - `himalaya`
   - `nano-pdf`
   - `summarize`
   - `wacli`
   - `goplaces`
8. 持續選 **No**（大約四次）
9. **Enable hooks** 選 `session-memory`（推薦）
10. **How do you want to hatch your bot** 選 `Hatch in TUI`

完成以上步驟後即安裝完畢 🎉

---

## 3. 啟動服務

### 啟動 Gateway

```bash
npx openclaw gateway
```

### 開啟 Dashboard（控制介面）

```bash
npx openclaw dashboard
```
