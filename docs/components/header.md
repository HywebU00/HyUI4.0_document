# Header 頁首

檔案名稱：sass/modual/\_header.scss
檔案名稱：sass/modual/\_menu.scss

<font color="#EE428B">頁首</font> 由 <font color="#EE428B">header</font> 標籤包覆，目前已預先設定 <font color="#EE428B">h1 (logo 圖檔)</font> 、 <font color="#EE428B">navigation</font> 、 <font color="#EE428B">search</font> 、 <font color="#EE428B">menu</font>等元素。

內含預設模組可參考

- <font color="#009ee7">Navigation 導覽列</font>
- <font color="#009ee7">Search 搜尋</font>
- <font color="#009ee7">Menu 主選單</font>

以下模組依照無障礙 <font color="#EE428B">tab</font> 遊走順序擺放，如無特殊需求，皆依照由上到下、由左到右之順序呈現。

頁首模組皆已設定響應式風格樣式，目前斷點預設為 <font color="#EE428B">768px</font> ，如需要更改斷點，請至 <font color="#EE428B">main.js</font>更改斷點變數，以及 <font color="#EE428B">\_valuable.scss</font> 更改斷點變數。

## HTML 範本

```html
<!-- header Start -->
<header class="header">
  <div class="container">
    <a class="accessKey" href="#aU" id="aU" accesskey="U" title="網站標題" tabindex="2">:::</a>
    <!-- navigation Start -->
    <nav class="navigation" role="navigation" aria-label="Site">
      <!-- 新增div navList -->
      <div class="navList">
        <ul>
          <li><a href="#">回首頁</a></li>
          <li><a href="#">網站導覽</a></li>
          <li><a href="#">English</a></li>
          <li><a href="#">常見問答</a></li>
        </ul>
      </div>
      <!-- fontSize -->
      <div class="fontSize">
        <span>字型大小：</span>
        <ul>
          <li><a role="button" href="#" class="small">小</a></li>
          <li><a role="button" href="#" class="medium">中</a></li>
          <li><a role="button" href="#" class="large">大</a></li>
        </ul>
      </div>
      <!-- language -->
      <div class="language">
        <a role="button">語言選擇</a>
        <ul>
          <li><a href="#">繁體中文</a></li>
          <li><a href="#">简体中文</a></li>
          <li><a href="#">ENGLISH</a></li>
        </ul>
      </div>
    </nav>
    <!-- navigation End -->
    <h1>
      <a href="index.html"><img src="images/logo.png" alt="網站標題" /></a>
    </h1>
    <!-- Search Start -->
    <div class="search" role="search">
      <div class="formGrp">
        <label for="mustSameAsId">搜尋</label>
        <input name="username" id="mustSameAsId" type="text" placeholder="請輸入文字" accesskey="S" title="請輸入文字" aria-label="搜尋網站內容" />
        <button type="button" class="btn btnSearch">查詢</button>
      </div>
      <div class="btnGrp">
        <button type="button" class="btn">進階搜尋</button>
      </div>
      <div class="keywordHot">
        <ul>
          <li><a href="#">熱門熱門</a></li>
          <li><a href="#">查詢</a></li>
          <li><a href="#">字詞三</a></li>
        </ul>
      </div>
    </div>
    <!-- Search End -->
    <!-- noscript -->
    <noscript>
      您的瀏覽器不支援JavaScript語法，JavaScript語法並不影響內容的陳述。您可使用按鍵盤上的Ctrl鍵+ (+)鍵放大/(-)鍵縮小來改變字型大小；回到上一頁可使用瀏覽器提供的 Alt+左方向鍵(←) 快速鍵功能；列印可使用瀏覽器提供的(Ctrl+P)功能。您的瀏覽器，不支援script語法，若您的瀏覽器無法支援請點選此超連結
      <a href="#">網站導覽</a>
    </noscript>
    <!-- menu Start -->
    <nav class="menu mainMenu" role="navigation" aria-label="About page">
      <ul>
        <li>
          <a href="#">第一層選單</a>
          <ul>
            <li><a href="#">第二層選單</a></li>
            <li><a href="#">第二層選單</a></li>
            <li><a href="#">第二層選單</a></li>
            <li><a href="#">第二層選單</a></li>
          </ul>
        </li>
        <li><a href="http://www.google.com">第一層有連結</a></li>
        <li>
          <a href="http://www.google.com">第一層有連結</a>
          <ul>
            <li><a href="http://www.google.com">第二層有連結</a></li>
            <li><a href="#">第二層選單</a></li>
            <li><a href="#">第二層選單</a></li>
            <li><a href="#">第二層選單</a></li>
            <li>
              <a href="#">第二層選單</a>
              <ul>
                <li><a href="http://www.google.com">第三層有連結</a></li>
                <li><a href="#">第三層選單</a></li>
                <li><a href="#">第三層選單</a></li>
                <li><a href="#">第三層選單</a></li>
                <li><a href="#">第三層選單</a></li>
                <li><a href="#">第三層選單</a></li>
                <li><a href="#">第三層選單</a></li>
                <li><a href="#">第三層選單</a></li>
              </ul>
            </li>
            <li><a href="#">第二層選單</a></li>
            <li><a href="#">第二層選單</a></li>
            <li><a href="#">第二層選單</a></li>
          </ul>
        </li>
        <li>
          <a href="#">第一層選單</a>
          <ul>
            <li><a href="#">第二層選單</a></li>
            <li><a href="#">第二層選單</a></li>
            <li>
              <a href="http://www.google.com">第二層有連結</a>
              <ul>
                <li>
                  <a href="http://www.google.com">第三層選單有下層</a>
                  <ul>
                    <li><a href="#">第四層選單</a></li>
                    <li><a href="#">第四層選單</a></li>
                  </ul>
                </li>
                <li>
                  <a href="http://www.google.com">第三層選單有連結</a>
                </li>
                <li><a href="#">第三層選單</a></li>
              </ul>
            </li>
            <li><a href="#">第二層選單</a></li>
          </ul>
        </li>
        <li>
          <a href="#">第一層選單</a>
          <ul>
            <li><a href="#">第二層選單</a></li>
            <li><a href="#">第二層選單</a></li>
            <li><a href="#">第二層選單</a></li>
            <li><a href="#">第二層選單</a></li>
          </ul>
        </li>
        <li>
          <a href="#">第一層選單</a>
          <ul>
            <li><a href="#">第二層選單</a></li>
            <li><a href="#">第二層選單</a></li>
            <li>
              <a href="http://www.google.com">第二層有連結</a>
              <ul>
                <li>
                  <a href="http://www.google.com">第三層選單有下層</a>
                  <ul>
                    <li><a href="#">第四層選單</a></li>
                    <li><a href="#">第四層選單</a></li>
                  </ul>
                </li>
                <li>
                  <a href="http://www.google.com">第三層選單有連結</a>
                </li>
                <li><a href="#">第三層選單</a></li>
              </ul>
            </li>
            <li><a href="#">第二層選單</a></li>
          </ul>
        </li>
      </ul>
    </nav>
    <!-- menu End -->
  </div>
</header>
<!-- header End -->
```

<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>
