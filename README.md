# AndroidDev_CourseFinalPJ

#### 主題：星巴克會員與行銷管理 APP

---

### **1. APP架構與功能**

### 主頁面
1. 設計主畫面並配置按鈕導航。
2. 建立「會員登入與註冊」頁面，設定 Firebase Authentication。

**參考：**

- [Rushly/Navigation Components](https://github.com/Mahmud0808/Rushly)
- [Firebase Authentication 教程](https://www.youtube.com/watch?v=QAKq8UBv4GI&t=9s&ab_channel=CodesEasy&loop=0)

#### **會員管理頁面**
- **功能描述**：
  - 註冊/登入
  - 個人資料管理（包括聯絡方式、地址、生日等）
  - 會員等級及優惠資訊查詢
  - 點數餘額及交易紀錄查詢
- **技術需求**：
  - 前端採用 RecyclerView 動態顯示點數紀錄。
  - Firebase Authentication 進行會員註冊與登入驗證。
  - 會員資料儲存至 Firebase Realtime Database 或 Firestore。
  - 會員等級、優惠對應查詢 D1「會員資料庫」。

#### **門市資訊頁面**
- **功能描述**：
  - 門市查詢
  - 門市營業時間、聯絡資訊查詢
  - 加盟店聯繫資料展示
- **技術需求**：
  - 使用 Google Maps API 或 OpenStreetMap 進行地圖定位與門市篩選。
  - 門市資訊由 D3「門市資料庫」提供，定期同步更新。
  - 提供快速撥打聯繫電話功能。

#### **商品頁面**
- **功能描述**：
  - 菜單瀏覽
  - 商品詳細資訊展示（含中/英文說明）
  - 商品圖片展示
- **技術需求**：
  - 商品資訊存儲於 D5「商品資料庫」。
  - 使用 Glide 庫優化圖片加載，提升流暢度。
  - 分類菜單採用 TabLayout + Fragment 實現動態切換。

#### **優惠活動頁面**
- **功能描述**：
  - 查看最新活動資訊
  - 活動註冊/參與
- **技術需求**：
  - 優惠活動資訊從 D4「行銷活動資料庫」抓取。
  - 註冊活動後更新至 D1 會員資料庫，並同步行銷部門數據。
  - Firebase Cloud Messaging (FCM) 實現活動推播通知。

---

### **2. DFD 圖的功能與資料流對應分析**
![starbucks_Member_1_2_Part_DFD](https://github.com/user-attachments/assets/6bc09216-cbec-42a9-b863-b1f67d011fa7)
![starbucks_Stock_Stores_Sales__3_4_5_Part_DFD](https://github.com/user-attachments/assets/e4f51813-fedc-4c72-a365-f6a390f7ff6e)

根據 PDF 文件中的 DFD 圖，系統核心功能與資料流如下：
1. **會員資料管理**：
   - 資料流：會員輸入個人資料 → 儲存會員資料 → 會員驗證。
   - 資料來源：D1「會員資料庫」。
2. **點數處理**：
   - 資料流：點數查詢/異動 → 更新點數交易紀錄。
   - 資料來源：D2「點數交易紀錄」。
3. **門市資訊管理**：
   - 資料流：門市資訊查詢 → 從 D3 門市資料庫讀取。
4. **行銷活動規劃**：
   - 資料流：查詢活動/促銷方案 → 從 D4 行銷活動資料庫讀取。
5. **商品資訊管理**：
   - 資料流：商品查詢 → 從 D5 商品資料庫讀取。
---
## 3. 參考網址資料
### 1.

https://github.com/akrajilwar/Android-Login-And-Registration/tree/master

此儲存庫 `akrajilwar/Android-Login-And-Registration` 提供了一個使用 PHP、MySQL 和 SQLite 資料庫的 Android 登入和註冊系統。它包含了完整的系統開發教學，並提供登入、註冊、電子郵件驗證和首頁的範例畫面。該儲存庫包含在 Windows 的 XAMPP 和網頁託管環境中設置系統的步驟，詳細說明了必要的配置和資料庫設置。

更多詳細資訊，您可以閱讀[README](https://github.com/akrajilwar/Android-Login-And-Registration/blob/65457e7f4e372518f7520f088078ca351ce98664/README.md)檔案。

### 2.

儲存庫 [Mahmud0808/Rushly](https://github.com/Mahmud0808/Rushly) 是一個使用 Kotlin 和 MVVM 架構建立的電子商務 Android 應用程式。它提供了時尚的介面、簡易的導航和流暢的購物瀏覽體驗。該應用程式使用 Firebase 服務實現身份驗證、Firestore 資料庫和儲存等功能。

更多詳細資訊，您可以查看[README檔案](https://github.com/Mahmud0808/Rushly/blob/9afb8afc12e6443f2499c19014afaeff79a7c292/README.md)。

### 3.

[YouTube: Login and Registration using Firebase in Android](https://www.youtube.com/watch?v=QAKq8UBv4GI&t=9s&ab_channel=CodesEasy&loop=0)

Firebase 是 Google 對 Android 手機開發的資料庫系統。