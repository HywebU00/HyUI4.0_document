# HTML 範本

```html
<!doctype html>
<html lang="zh-Hant" class="no-js">

<head>
    <meta name="robots" content="noindex" />
    <!-- 使用 noindex 禁止 Google 搜尋建立索引，套版時請工程師刪掉這行 -->
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>HyUI kit</title>

    <!-- style css -->
    <link rel="stylesheet" href="css/style.css" />
    <!-- favicon -->
    <link href="images/favicon.png" rel="icon" type="image/x-icon" />
</head>
<body>

    <!-- lazyload -->
    <script src="vendor/lazyload/lazyload.js"></script>
    <!-- picturefill -->
    <script src="vendor/picturefill/picturefill.min.js" async></script>
    <!-- fancybox -->
    <script src="vendor/fancybox/fancybox.js"></script>
    <!-- swiper -->
    <script src="vendor/swiper/swiper-bundle.min.js"></script>
    <!-- main js-->
    <script src="js/main.js"></script>
    <!-- js -->
    <script src="js/customize.js" type="module"></script>
</body>
</head>

```

---

## 設定網頁的語系

設定網頁的語系 讓瀏覽器能更正確解析與編碼

```html
<!DOCTYPE html>
<html lang="zh-Hant" class="no-js"></html>
```

HTML 的 `lang` 屬性可用於網頁或部分網頁的語言。這對搜索引擎和瀏覽器是有幫助的。 根據 W3C 推薦標準，應該通過 `<html>`標籤中的 `<lang>`屬性對每張頁面中的主要語言進行聲明。相關資料請參考 [W3C Language Codes](https://www.w3schools.com/tags/ref_language_codes.asp)。

| 常見語系                       | 對應設定       |
| :----------------------------- | :------------- |
| English                        | lang='en'      |
| 繁體中文 Chinese (Traditional) | lang='zh-Hant' |
| 簡體中文 Chinese (Simplified)  | Text           |

為了無障礙於關閉 Javascript 的檢測，請先預留此`class="no-js"` 的設定。更多內容請參考`無障礙單元`。

---

## head 內容

```html
<meta charset="utf-8" />
<meta http-equiv="X-UA-Compatible" content="IE=edge" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>HyUI kit</title>
<!-- hyUI css -->
<link rel="stylesheet" href="css/style.css" />
<!-- favicon -->
<link href="images/favicon.png" rel="icon" type="image/x-icon" />
```

`<meta http-equiv="X-UA-Compatible" content="IE=edge">` 預設指定 IE 瀏覽器按照最高的標準模式解析頁面。

`<meta name="viewport" content="width=device-width, initial-scale=1,shrink-to-fit=no">`預設畫面載入初始縮放比例 100%。

`shrink-to-fit=no`這個屬性為 iOS 9 能新辨認的屬性：shrink-to-fit 並設定為 no，這設定可以讓網頁的寬度自動適應手機螢幕的寬度。

以下兩種設定都可以防止使用者做畫面縮放，將畫面鎖在縮放比例 100%

```html
<meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1, maximum-scale=1" />
```

```html
<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no" />
```

## 載入 CSS

範本已先預設匯入`style.css`

```html
<link rel="stylesheet" href="css/style.css" />
```

---

## body 內容

`<body>`預設已存在"回頁首"的按鈕，但這只是一個範例。hyUI 並無預設任何文本才能執行，只需要針對開發所需，可參考本網站提供之範例自由組合，或是自行開發都是彈性的。

```html
<a href="#" class="scrollToTop">回頁首</a>
```

---

## JavaScript

範本已先預設匯入下列 JavaScript 檔案，可根據需求增減刪除。

```html
<!-- lazyload -->
<script src="vendor/lazyload/lazyload.js"></script>
<!-- picturefill -->
<script src="vendor/picturefill/picturefill.min.js" async></script>
<!-- fancybox -->
<script src="vendor/fancybox/fancybox.js"></script>
<!-- swiper -->
<script src="vendor/swiper/swiper-bundle.min.js"></script>
<!-- main js-->
<script src="js/main.js"></script>
<!-- js -->
<script src="js/customize.js" type="module"></script>
```

## 外掛請放入 vendor 資料夾

> 範例: 匯入 lazyload.js

是一款可以將圖片延遲載入網頁的`JavaScript`套件，主要功能可以減少伺服器多餘的流量輸出/減輕伺服器負擔及提高使用者體驗。它會依照用戶在滾動頁面時當用戶快要滾動到圖片時才開始跟伺服器請求這張圖片下來，然後即時顯示給用戶觀看。

```html
<script src="vendor/lazyload/lazyload.js"></script>
```

> 範例: 匯入 picturefill.min.js

它則是透過 html5 的 picture 的標籤，來實現在不同的裝置的解析，載入相對應的圖檔大小，如此一來在 3G 吃不飽，4G 又不穩的情況下，對於使用者來說真是一大福音，而目前這個方法是用 JS 來進行切換，因此在製作圖檔時，就多存幾個檔案即可解決。

```html
<script src="vendor/picturefill/picturefill.min.js" async></script>
```

## 匯入 main.js

預設提供常用之互動模組，例如：lightbox、menu 等效果，例如：無障礙檢測 `tab`鍵盤操作瀏覽網頁之設定。如果沒有特殊的版本更新需求，請不任意新增或刪除 `style.js` 的預設設定。

```html
<script src="js/main.js"></script>
```

## 自行撰寫之 JavaScript 效果

可自行撰寫所需要的互動程式，可寫在 `customize.js`
當禁用 JavaScript 時，請視情況於網頁顯示`<noscript>`，並標記上相關說明文字。

```xml
<script src="js/customize.js"></script>
```
