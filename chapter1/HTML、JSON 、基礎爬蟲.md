---
tags: 網頁開發 爬蟲
---
# HTML、JSON 、基礎爬蟲

###### tags: `網頁開發` `爬蟲`

## 1.1 認識HTML
HTML : 標籤 + 屬性

```=
<!DOCTYPE html>                                  #告訴瀏覽器html版本
<html lang="zh">                                 #<html>標籤 ；lang= 屬性
<head>                   
<meta charset="utf-8">                           #設定網頁編碼，UTF-8 是萬國碼
<title>網頁標題</title>
</head>
<body text="blue">
網頁內容
</body>
</html>
```

## 1.2 認識JSON

使用大括號定義成對的鍵和值(Key-value Pairs)
```=
{
   "key1":"value1",
   "key2":"value2",
   "key3":"value3",
   ...
}

```

```=
[                                  #定義物件陣列

    {                              #定義物件1
       "key1":"value1",
       "key2":"value2"
 
    }                              #定義物件1
    
    {                              #定義物件2
       "key1":"value1",
       "key2":"value2"
 
    }                              #定義物件2

]                                  #定義物件陣列

```
## 1.3 網路爬蟲

* 針對目標網站自動擷取資訊的技術
* 用途:
    * 取得競爭者商品價格
    * 取得評價
    * 追蹤相關資訊 
### 為什麼需要爬蟲?

減少大量重複的動作

### 爬蟲的基本步驟

* 識別出目標網址
* 送出HTTP請求取得網頁
* 分析HTML
* 取出所需資料

## 1.4 網路爬蟲使用的相關技術

### 1.4.1 網路爬蟲使用的相關技術
#### HTTP通訊協定
![](https://i.imgur.com/z207ckW.png)

#### 常見三種方式定位網頁資料
* CSS
* Xpath
* Regular Expression : 搭配CSS進行字串比對


### 1.4.2 瀏覽網頁的步驟
* 輸入網址
* 伺服器回傳網頁標籤內容
* 剖析建立DOM節點數

### 1.4.3 網址的組成

**http://example.com:80/test/?user=hueyan**
* http : 通訊協定
* example.com : 網域名稱會透過DNS轉換成IP位置
* 80 : port 
* /test : 請求的路徑
* ?user=hueyan : ?後面傳遞查詢的參數，&來串接多個參數

## 1.5 網路爬蟲使用的相關函式庫


* HTTP : Requests
* 靜態 : Beautiful Soup 、 lxml
* 動態 : Selenium
* 整個網站 : Scrapy
