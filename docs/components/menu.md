# Menu 主選單

?>檔案名稱：sass/module/`_menu.scss`<br>
檔案名稱：sass/module/`_megamenu.scss`

**主選單標籤**為`nav.menu`及`nav.megamenu`([範例](https://hywebu00.github.io/HyUI_v4.0/mp_megamenu.html#))目前預設為最多`4`層，mainMenu 為判斷使用必須保留。

主選單在手機版預設放置於畫面左方`sidebar`，手機版會自動產生選單按鈕，用於打開收合左側選單。

## Menu HTML 範本

```html
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
            <li><a href="http://www.google.com">第三層選單有連結</a></li>
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
        <li><a href="#">第二層選單</a></li>
        <li><a href="#">第二層選單</a></li>
      </ul>
    </li>
  </ul>
</nav>
<!-- menu End -->
```

## Megamenu HTML 範本

```html
<!-- megamenu Start -->
<nav class="megaMenu mainMenu" role="navigation" aria-label="About page">
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
        <li><a href="#">第二層選單</a></li>
        <li><a href="#">第二層選單</a></li>
        <li><a href="#">第二層選單</a></li>
        <li><a href="#">第二層選單</a></li>
      </ul>
    </li>
    <li>
      <a href="#">第一層選單</a>
      <ul>
        <li>
          <a href="#">第二層選單</a>
          <ul>
            <li><a href="http://www.google.com">第三層選單有下層</a></li>
            <li><a href="http://www.google.com">第三層選單有連結</a></li>
            <li><a href="#">第三層選單</a></li>
            <li><a href="#">第三層選單</a></li>
            <li><a href="#">第三層選單</a></li>
          </ul>
        </li>
        <li>
          <a href="#">第二層選單</a>
          <ul>
            <li><a href="http://www.google.com">第三層選單有下層</a></li>
            <li><a href="http://www.google.com">第三層選單有連結</a></li>
            <li><a href="#">第三層選單</a></li>
          </ul>
        </li>
        <li>
          <a href="http://www.google.com">第二層有連結</a>
          <ul>
            <li>
              <a href="http://www.google.com">第三層選單有下層</a>
              <ul>
                <li><a href="#">第四層選單第四層選單</a></li>
                <li><a href="#">第四層選單</a></li>
              </ul>
            </li>
            <li><a href="http://www.google.com">第三層選單有連結</a></li>
            <li><a href="#">第三層選單</a></li>
          </ul>
        </li>
        <li><a href="#">第二層選單</a></li>
        <li>
          <a href="#">第二層選單</a>
          <ul>
            <li><a href="http://www.google.com">第三層選單有下層</a></li>
            <li><a href="http://www.google.com">第三層選單有連結</a></li>
            <li><a href="#">第三層選單</a></li>
            <li><a href="#">第三層選單</a></li>
            <li><a href="#">第三層選單</a></li>
          </ul>
        </li>
        <li>
          <a href="#">第二層選單</a>
          <ul>
            <li><a href="http://www.google.com">第三層選單有下層</a></li>
            <li><a href="http://www.google.com">第三層選單有連結</a></li>
            <li><a href="#">第三層選單</a></li>
          </ul>
        </li>
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
            <li><a href="http://www.google.com">第三層選單有連結</a></li>
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
        <li><a href="#">第二層選單</a></li>
        <li><a href="#">第二層選單</a></li>
      </ul>
    </li>
  </ul>
</nav>
<!-- megamenu End -->
```
