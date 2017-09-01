# 個人資訊
- 張家峻/男/25 years
- 台灣科技大學/資訊工程系/學士
- 工作年資：1年
- github：https://github.com
- email：chiachun0920@gmail.com
- 期望職位：前端工程師、後端工程師

# 工作經歷

## 中國附醫資訊室 (2016/09-*)

在這裡我擔任程式設計師，大部分時間負責web前端的部分，偶而支援後端

### **腦中風評估系統**

在這個專案我負責前端畫面的部分(使用Angular 2.0 framework)，

這個評估系統有大量的表單需要載入，而這些載入又牽扯到一些非同步執行的問題，

經過一番考慮後，我決定將有限狀態機(FSM)加入系統，

並透過FSM來管理複雜的狀態，來減少因為非同步問題而產生出的各種bug，

最後這個專案順利通過評鑑，並獲得醫師們不少好評

### **電子表單簽核流程**

這專案我一樣負責前端部分，這個系統困難點就是
- 各式各樣電子表單會在不同的系統重複使用及出現，必須重視**重用性**
- 數以百張的表單在程式初期載入會拖垮速度

為了重用性，我寫了一個框架來載入所有的表單，並讓其他系統來共用所有表單

為了不讓執行初期的載入動做拖垮速度，我研究了Angular提供的Lazy module load的技術，

實際加入後，成功降低載入時間，

最後這個專案在時程的壓力下，成功上線運行。

![123](http://i.imgur.com/U8np8dP.png)

# 開源作品集

- ccc-ui：為了日後開發網站需要而開發一些比較常用及特殊的UI，以Angular來撰寫
    - demo : https://chiachun0920.github.io/ccc-ui/
    - source code : https://github.com/chiachun0920/ccc-ui

# 學生時期作品

- https://goo.gl/38eSvG (作品集)
- https://goo.gl/bMyZi6 (漢宮熱舞跳舞機-影片)

# 使用的技術清單
- Web前端：
    - CSS、Html、Javascript
    - Angular 4.0
    - Rxjs
- Web後端：
    - Node.js
    - express

























