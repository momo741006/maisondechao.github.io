# 🌈 虹靈御所八字系統 - maisondechao.com 部署指南

## 🎯 **目標**
將虹靈御所八字人生兵法系統部署到您的專屬域名 **`maisondechao.com`** 上，使用免費的GitHub Pages託管服務。

## 📦 **準備文件**
- `maisondechao-github-ready.tar.gz` - 完整專案壓縮包
- `index.html` - 虹靈御所八字系統主文件
- `CNAME` - 自定義域名配置文件
- `README.md` - 專案說明文件

## 🚀 **部署步驟**

### **第一步：創建GitHub儲存庫**

1. **登入GitHub**
   - 前往 [github.com](https://github.com)
   - 登入您的GitHub帳號

2. **創建新儲存庫**
   - 點擊右上角的 "+" 號
   - 選擇 "New repository"
   - **儲存庫名稱**：`maisondechao` 或 `maisondechao.github.io`
   - **設為Public**（公開）
   - **不要**勾選 "Add a README file"（我們已經準備好了）
   - 點擊 "Create repository"

### **第二步：上傳專案文件**

**方法A：網頁上傳（推薦）**
1. 在新建的儲存庫頁面，點擊 "uploading an existing file"
2. 解壓縮 `maisondechao-github-ready.tar.gz`
3. 將以下文件拖拽到上傳區域：
   - `index.html`
   - `CNAME`
   - `README.md`
4. 在Commit訊息中輸入：`🌈 部署虹靈御所八字系統到 maisondechao.com`
5. 點擊 "Commit changes"

**方法B：Git命令行**
```bash
# 解壓縮專案文件
tar -xzf maisondechao-github-ready.tar.gz
cd maisondechao-github

# 添加GitHub儲存庫
git remote add origin https://github.com/您的用戶名/maisondechao.git

# 推送到GitHub
git branch -M main
git push -u origin main
```

### **第三步：啟用GitHub Pages**

1. **進入儲存庫設置**
   - 在儲存庫頁面，點擊 "Settings" 標籤
   - 在左側選單找到 "Pages"

2. **配置Pages設置**
   - 在 "Source" 下拉選單選擇 "Deploy from a branch"
   - 選擇 "main" 分支
   - 資料夾選擇 "/ (root)"
   - 點擊 "Save"

3. **確認自定義域名**
   - 在 "Custom domain" 欄位應該會自動顯示 `maisondechao.com`
   - 如果沒有，請手動輸入 `maisondechao.com`
   - 勾選 "Enforce HTTPS"
   - 點擊 "Save"

### **第四步：配置DNS設置**

**重要：您需要在您的域名提供商處設置DNS記錄**

1. **登入您的域名管理面板**（如GoDaddy、Namecheap、Cloudflare等）

2. **添加以下DNS記錄**：

   **A記錄（指向GitHub Pages的IP）**：
   ```
   類型: A
   名稱: @（或留空）
   值: 185.199.108.153
   ```
   ```
   類型: A
   名稱: @（或留空）
   值: 185.199.109.153
   ```
   ```
   類型: A
   名稱: @（或留空）
   值: 185.199.110.153
   ```
   ```
   類型: A
   名稱: @（或留空）
   值: 185.199.111.153
   ```

   **或者使用CNAME記錄（二選一）**：
   ```
   類型: CNAME
   名稱: www
   值: 您的用戶名.github.io
   ```

3. **等待DNS生效**
   - DNS更新通常需要幾分鐘到24小時
   - 可以使用 [whatsmydns.net](https://www.whatsmydns.net/) 檢查DNS傳播狀態

### **第五步：驗證部署**

1. **等待GitHub Pages構建**
   - 回到GitHub儲存庫的 "Actions" 標籤
   - 等待綠色勾號表示構建成功

2. **訪問您的網站**
   - 前往 `https://maisondechao.com`
   - 應該能看到虹靈御所八字系統

3. **測試功能**
   - 點擊「載入範例」
   - 測試八字計算功能
   - 確認所有模塊正常運作

## ✅ **預期結果**

部署成功後，您將擁有：
- **專屬網址**：`https://maisondechao.com`
- **SSL證書**：自動HTTPS加密
- **全球CDN**：快速訪問速度
- **免費託管**：GitHub Pages永久免費

## 🌟 **網站功能**

您的 `maisondechao.com` 將包含：
- ✅ 四時軍團系統（家族/成長/本我/未來兵團）
- ✅ 完整十神顯示（每柱最多4個十神）
- ✅ 22個神煞系統
- ✅ 早子時/晚子時計算選項
- ✅ 資料驅動故事生成
- ✅ 虹靈漸變主題設計
- ✅ 響應式設計（手機/電腦完美適配）
- ✅ 星空背景動畫效果

## 🔧 **故障排除**

### **常見問題**

1. **網站顯示404錯誤**
   - 確認文件名為 `index.html`
   - 檢查GitHub Pages是否已啟用
   - 等待幾分鐘讓GitHub重新構建

2. **自定義域名無法訪問**
   - 檢查DNS設置是否正確
   - 等待DNS傳播完成（最多24小時）
   - 確認CNAME文件內容為 `maisondechao.com`

3. **HTTPS證書問題**
   - 取消勾選 "Enforce HTTPS"，等待幾分鐘後重新勾選
   - 確保DNS設置正確

4. **功能異常**
   - 檢查瀏覽器控制台是否有錯誤
   - 清除瀏覽器快取
   - 嘗試無痕模式訪問

### **聯繫支援**
如果遇到任何問題，請提供：
- 具體的錯誤訊息
- 瀏覽器控制台截圖
- DNS設置截圖

## 🎉 **恭喜！**

完成以上步驟後，您的虹靈御所八字系統就會在 `https://maisondechao.com` 上線運行！

這將是一個專業、美觀、功能完整的命理分析平台，完美展現傳統文化與現代技術的結合。

---

**祝您部署順利！如有任何問題，隨時聯繫我們。** 🌟

