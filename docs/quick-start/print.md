# 無障礙(Accessibility)與列印

## 支持無障礙 2.0 AA 等級

?>針對國家通訊傳播委員會頒布之網站無障礙規範 2.0 版，其中許多規範會影響到網站開發者處理無障礙的設定，讓無障礙檢測都能透過鍵盤使用，`HyUI` 在 `SASS` 及 `main.js` 已經針對「連結」、「選單操作」...等預先調整了相關的設定，目前是以無障礙 2.0AA 版本為基礎。

!>注意 :zap:
無障礙以機器檢測與人工檢測為準，HyUI 只能預先處理基礎樣式，如遇到客製專案需求開發，仍需靠開發人員共同處理。

## 快速鍵設定

本網站依 **無障礙網頁設計原則** 建置，網站的主要內容分為 **三大區塊**：

1.  上方功能區塊、 2. 中央內容區塊、 3.下方功能區塊。

- **Alt+U**：上方功能區塊，包括回首頁、網站導覽、網站搜尋、字體選擇、版本選擇等。
- **Alt+C**：中央內容區塊，為本頁主要內容區。
- **Alt+Z**：下方功能區塊。
- **Alt+S**：網站搜尋。

> 如果您的瀏覽器是 `Firefox`，快速鍵的使用方法是 `Shift+Alt+(快速鍵字母)`，例如 `Shift+Alt+C `會跳至網頁中央區塊，以此類推。

![](https://i.imgur.com/bpztC6e.png ':size=300')

?> **當本網站項目頁籤無法以滑鼠點選時，您可利用以下鍵盤操作方式瀏覽資料** <br>
`←` `→` or`↑` `↓`：按**左右鍵**或**上下鍵**移動標籤順序。<br>
`Home` or `End` `→`：可直接**跳至標籤第一項**或者**最後一項**。<br>
`Tab`：停留於該標籤後,可利用 **Tab** 鍵跳至內容瀏覽該筆資料，遇到 **radio** 按鈕時請配合使 `←` `→` or`↑` `↓`鍵移動項目順序。<br>
`Tab + Shift`：按 `Tab + Shift` 可往**回跳至上一筆資料**；當跳回至標籤項目時您可繼續利用`←` `→` or`↑` `↓` 鍵移動標籤順序。

```html
<!-- 直接跳主內容區 -->
<a class="goCenter" href="#center" tabindex="1">按Enter到主內容區</a>
```

## 快捷錨點設定

目前提供之頁面範本，已先置入相對應位置，但可依照專案另外做客製化設定。

```html
<!-- 網站標題區 -->
<a class="accessKey" href="#aU" id="aU" accesskey="U" title="網站標題" tabindex="2">:::</a>
<!-- 網站搜尋 (放置input輸入框) -->
<input name="username" id="mustSameAsId" type="text" placeholder="請輸入文字" accesskey="S" title="請輸入文字" aria-label="搜尋網站內容" />
<!-- 主要內容區 -->
<a class="accessKey" href="#aC" id="aC" accesskey="C" title="主要內容區">:::</a>
<!-- 頁尾區 -->
<a class="accessKey" href="#aZ" id="aZ" accesskey="Z" title="頁尾區">:::</a>
```

## JavaScript 設定

```javascript
// -----------------------------------------------------------------------
// -----  無障礙快捷鍵盤組合 a11yKeyCode   ----------------------------------
// -----------------------------------------------------------------------

function a11yKeyCode() {
  let search = document.querySelector('.search input[type="text"]');
  let header = document.querySelector('.header .accessKey');
  let main = document.querySelector('.main .accessKey');
  let footer = document.querySelector('footer .accessKey');
  let distance = 0;

  // --- focus element
  function focusElem(distance, el) {
    if (window.scrollY === distance) {
      el.focus();
    }
  }

  // --- scroll to element position
  function scrollAnime(distance, el) {
    window.scrollTo({
      top: distance,
      behavior: 'smooth',
    });
    window.addEventListener('scroll', () => {
      focusElem(distance, el);
    });
  }

  // --- click a11 button
  document.addEventListener('keydown', (e) => {
    switch (e.altKey && e.code) {
      // alt+S 查詢
      case true && 'KeyS':
        scrollAnime(0, search);
        focusElem(0, search);
        break;
      // --- alt+U header
      case true && 'KeyU':
        scrollAnime(0, header);
        focusElem(0, header);
        break;
      // --- alt+C 主要內容區
      case true && 'KeyC':
        main.focus();
        let _headerHeight = document.querySelector('header').offsetHeight;
        scrollAnime(_headerHeight, main);
        focusElem(_headerHeight, main);
        break;
      // --- alt+Z footer
      case true && 'KeyZ':
        let _bodyScrollHeight = document.documentElement.scrollHeight;
        let _bodyClientHeight = document.documentElement.clientHeight;
        let _distance = _bodyScrollHeight - _bodyClientHeight;
        scrollAnime(_distance, footer);
        focusElem(_distance, footer);
        break;
    }
  });
}
a11yKeyCode();
```

## 列印

列印樣式，請於 `print.scss`編寫 SCSS，同樣統一匯出於 `style.css` 內。

?>檔案名稱：檔案名稱：sass/common/`print.scss`

!>注意 :zap:媒體格式需使用`@media print`；如需要預覽，請於瀏覽器點選**列印 / 預覽列印** 檢視。

```sass
// 列印樣式
@media print {
    %no-bg {
        background: none;
    }
    /* -------------------------------不需要列印的區塊，請放置於這----//*/
    header,
    .fatfooter,
    footer,
    .accesskey,
    .submenu {
        display: none;
    }
   ....
   ....
   ....
        p {
            a {
                word-wrap: break-word;
            }
            a[href^="http"]:after {
                content: " ("attr(href) ")";
                font-size: 90%;
            }
            a[href^="#"]:after {
                display: none;
            }
        }
        abbr[title]:after {
            content: " ("attr(title) ")";
        }
        table {
            background: #FFF;
        }
        li {
            content: "» ";
        }
    }
}
```
