# 個人資訊
- 張家峻/男/28 years
- 台灣科技大學/資訊工程系/學士
- 工作年資：3年
- github：https://github.com/chiachun0920
- email：chiachun0920@gmail.com
- 期望職位：後端工程師

## 關於我

> Cloud developer (familiar with AWS and python) and solution provider

>喜歡思考事情的本質，如果是我我會如何設計，並試著簡單地解釋給其他人聽懂

## 技術 stack
1. AWS
    - VPC
    - EC2
    - SQS
    - Lambda
    - Api Gateway
2. python
    - django framework
3. serverless framework
4. vuejs

# 工作經歷

## 國泰金控 (* - *)

### 做了什麼

1. 打造 OAuth 服務，目的是為了整合各個子公司的資源，以統一的會員系統來提供
2. 以 lambda + apigateway 建立與整合其他 component team 的 API (apihub)，並提供給外部通路使用
3. 開發維護會員系統(目前會員數為 150萬)
    - 設計＆開發 single sign on(單點登入) 機制
    - 使用者授權機制
    - 權限控管機制
4. 以 business rule 搭配 lambda 及 sqs 設計出一個商業邏輯引擎，目的是為了符合日益俱增的行銷需求
5. 設計＆開發貼標系統，各通路的權限控管，開放 api 給其他通路串接使用

### 遇到的挑戰
1. lambda 
    1. cold start
        1. warm up
        2. provisioned concurrency
    2. applicant: step function with many lambda
        1. reduce total response duration from 20s to 700ms
2. upgrade legacy membership data
    1. old data is insecure
    2. find solution to upgrade data to make it securable
3. high through traffic of api server
    1. read and write split
    2. using aurora cluster
4. content type solution
    1. avoid large table migration frequently
5. API Hub using two layer architecutre
    1. Cost (one api with two lambda invocation)
    2. Duration
    3. lambda concurrency usage
    4. different ORM
        1. define model using Django ORM
        2. Need to replicate model definition as similar as possible
    5. Solution:
        1. build out Django orm as sdk
        2. publish SDKs to lambda layer
        3. using Django to build out a api server
        4. deploy Django wsgi to serverless framework

## 雲發互動科技 (2017/11 - *)

在這裡我擔任全端工程師，負責維護網站後台及 API 開發。

### **巨量資料匯出**

這樣的 API 會遇到的挑戰就是容易造成 server loading 過重，不管是 db 或是 instance

所以面對這樣的問題採用了 amqp 當作 message broker，將 mission 發出去給其他 worker 處理。

最後透過 s3 sdk 以串流的方式上傳到 aws s3 bucket,

成功降低 api server 的負擔。

### **Batch API**

為了提升前端取資料的效能，我們將許多的 API 包裝處理，以 message dispatch 的方式交由 worker 來消化

並搭配 amqp rpc model 來取得 worker 的處理結果，

達成 One request, all response, 成功降低 前端取得資料的 transmission time


### **維護 no8 console**

使用了 Angular 搭配 Parse sdk 來開發，上線一年多的時間經歷過多次改版，

大量使用 Rxjs 來 解決非同步訊息傳輸的問題，

且透過 Nativescript 這樣的框架，來快速上架 mobile application。

## 中國附醫資訊室 (2016/09-2017/10)

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

# 開源作品集

- ccc-ui：為了日後開發網站需要而開發一些比較常用及特殊的UI，以 Angular 來撰寫
    - demo: https://chiachun0920.github.io/ccc-ui/
    - source code: https://github.com/chiachun0920/ccc-ui 
- retryp: function to retry promise if encountering an error, and return promise.
    - source code: https://github.com/chiachun0920/retryp
- efficient-scheduler: Schedule a timeout job by efficiently using setTimeout
    - source code: https://github.com/chiachun0920/efficient-timeout

# 學生時期作品

- https://goo.gl/38eSvG (作品集)
- https://goo.gl/bMyZi6 (漢宮熱舞跳舞機-影片)

# 使用的技術清單
- Web前端：
    - CSS、Html、Javascript
    - Angular
    - Rxjs
- Web後端：
    - Node.js
    - Parse server
    - mongo
    - aws console
    - docker























