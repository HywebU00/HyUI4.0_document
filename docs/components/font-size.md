# Font-Size / 控制文章字體大小

?>檔案名稱：sass/ module / `functionPanel.scss`<br>
檔案名稱：sass/element/`font.scss`<br>

!> 注意 :zap: font-size 模組需搭配頁面上有文章內容作切換呈現，可用 `內容的部分` 或 `需要網站全域` 字級控制，可自行到`customize.js`將選擇器改為 `innerPage`或 `body`即可。

<!-- 文字大小 -->
  <div class="fontSize">
    <span>字型大小：</span>
    <!-- 英文用<span>font-size：</span> -->
    <ul>
      <li><a role="button" href="javascript:;" class="small">小</a></li>
      <li><a role="button" href="javascript:;" class="medium">中</a></li>
      <li><a role="button" href="javascript:;" class="large">大</a></li>
    </ul>
  </div>

<!-- <iframe height="265" style="width: 100%;" scrolling="no" title="Font-Size / 控制文章字體大小" src="https://codepen.io/u00hyui/embed/wvJvqPx?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/wvJvqPx'>Font-Size / 控制文章字體大小</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe> -->

## SCSS 預設的文字大中小設定

> 可於 `_font.scss`設定文字的大小，預設為 `medium`適中字型 `1em` 大小，為網站的基本設定，因此只需要設定小、大的字級即可，目前字級大小設定設於`.innerPage`內，如有特殊需求，可自行修改預設值。

- 小型字體大小：0.938em(15px)
- 中型字體大小：1em(16px)
- 大型字體大小：1.125em(18px)

<!-- tabs:start -->

#### **HTML**

```html
<div class="fontSize">
  <span>字型大小：</span>
  <!-- 英文用<span>font-size：</span> -->
  <ul>
    <li><a role="button" href="#" class="small">小</a></li>
    <li><a role="button" href="#" class="medium">中</a></li>
    <li><a role="button" href="#" class="large">大</a></li>
  </ul>
</div>
```

#### **CSS**

```sass
body {
  font-size: 1em;
  // --變更為全站
  &.smallSize {
    font-size: 0.938em;
  }
  &.largeSize {
    font-size: 1.125em;
  }
}
```

#### **JavaScript**

```javascript
function jsAddClass(element, className) {
  if (element.classList) element.classList.add(className);
  else if (!hasClass(element, className)) {
    element.className += ' ' + className;
  }
}
function jsRemoveClass(element, className) {
  if (element.classList) element.classList.remove(className);
  else if (hasClass(element, className)) {
    let reg = new RegExp('(\\s|^)' + className + '(\\s|$)');
    element.className = element.className.replace(reg, ' ');
  }
}
function fontSize() {
  const el = document.querySelectorAll('.fontSize') || null; // --- 控制的對象
  const control = document.querySelector('body') || null; // --- 控制的對象名稱
  // --- 點擊文字大小按鈕
  el.forEach((i) => {
    i.querySelectorAll('a').forEach((i) => {
      // --- 移除 active 的 class 名稱
      function removeActiveClass() {
        const _parentEle = i.parentNode.parentNode;
        _parentEle.querySelectorAll('a').forEach((i) => {
          i.classList.remove('active');
        });
      }
      i.addEventListener('click', (e) => {
        removeActiveClass();
        createCookie('FontSize', `${e.target.className}`, 356);
        addChangeClass(e.target.className);
        jsAddClass(e.target, 'active');
      });
    });
  });
  function addChangeClass(targetName) {
    if (control === null) {
      return;
    }
    switch (targetName) {
      case 'small':
        control.classList.remove('largeSize', 'medium_size');
        control.classList.add('smallSize');
        break;
      case 'medium':
        control.classList.remove('smallSize', 'largeSize');
        control.classList.add('medium_size');
        break;
      case 'large':
        control.classList.remove('smallSize', 'medium_size');
        control.classList.add('largeSize');
        break;
    }
  }
  // --- 創造新的 字體大小設定
  function createCookie(name, value, days) {
    let _expires;
    const _date = new Date();
    if (days) {
      _date.setTime(_date.getTime() + days * 24 * 60 * 60 * 1000);
      _expires = '; expires=' + _date.toGMTString();
    } else {
      _expires = '';
    }
    document.cookie = name + '=' + value + _expires + '; path=/';
  }
  // --- 讀取瀏覽器上 字體大小設定
  function readCookie(name) {
    const value = `; ${document.cookie}`;
    const parts = value.split(`; ${name}=`);
    if (parts.length === 2) return parts.pop().split(';').shift();
  }
  // --- 初始化 字體大小設定
  window.onload = (e) => {
    const _cookie = readCookie('FontSize');
    // --- 如果沒有_cookie 則預設值為'medium'
    if (_cookie == null) {
      _cookie = 'medium';
    }
    document.querySelectorAll(`.${_cookie}`).forEach((i) => {
      i.click();
      e.preventDefault();
    });
  };
}
fontSize();
```

<!-- tabs:end -->

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<style>
  .fontSize a{
    color: #000 !important;
    font-weight: 400 !important;
  }
   .fontSize a.active{
    color:#fff !important;
  }
  .fontSize a:hover{
    color:#fff !important;
  }
  body.largeSize {
    font-size: 1.125em;
  }
  body.smallSize {
    font-size: 0.938em;
  }
  body{
     font-size: 1em;
  }
</style>
<script>
  function jsAddClass(element, className) {
  if (element.classList) element.classList.add(className);
  else if (!hasClass(element, className)) {
    element.className += ' ' + className;
  }
}
function jsRemoveClass(element, className) {
  if (element.classList) element.classList.remove(className);
  else if (hasClass(element, className)) {
    let reg = new RegExp('(\\s|^)' + className + '(\\s|$)');
    element.className = element.className.replace(reg, ' ');
  }
}
  function fontSize() {
  const el = document.querySelectorAll('.fontSize') || null; // --- 控制的對象
  const control = document.querySelector('body') || null; // --- 控制的對象名稱
  // --- 點擊文字大小按鈕
  el.forEach((i) => {
    i.querySelectorAll('a').forEach((i) => {
      // --- 移除 active 的 class 名稱
      function removeActiveClass() {
        const _parentEle = i.parentNode.parentNode;
        _parentEle.querySelectorAll('a').forEach((i) => {
          i.classList.remove('active');
        });
      }
      i.addEventListener('click', (e) => {
        removeActiveClass();
        createCookie('FontSize', `${e.target.className}`, 356);
        addChangeClass(e.target.className);
        jsAddClass(e.target, 'active');
      });
    });
  });
  function addChangeClass(targetName) {
    if (control === null) {
      return;
    }
    switch (targetName) {
      case 'small':
        control.classList.remove('largeSize', 'medium_size');
        control.classList.add('smallSize');
        break;
      case 'medium':
        control.classList.remove('smallSize', 'largeSize');
        control.classList.add('medium_size');
        break;
      case 'large':
        control.classList.remove('smallSize', 'medium_size');
        control.classList.add('largeSize');
        break;
    }
  }
  // --- 創造新的 字體大小設定
  function createCookie(name, value, days) {
    let _expires;
    const _date = new Date();
    if (days) {
      _date.setTime(_date.getTime() + days * 24 * 60 * 60 * 1000);
      _expires = '; expires=' + _date.toGMTString();
    } else {
      _expires = '';
    }
    document.cookie = name + '=' + value + _expires + '; path=/';
  }
  // --- 讀取瀏覽器上 字體大小設定
  function readCookie(name) {
    const value = `; ${document.cookie}`;
    const parts = value.split(`; ${name}=`);
    if (parts.length === 2) return parts.pop().split(';').shift();
  }
  // --- 初始化 字體大小設定
  window.onload = (e) => {
    const _cookie = readCookie('FontSize');
    // --- 如果沒有_cookie 則預設值為'medium'
    if (_cookie == null) {
      _cookie = 'medium';
    }
    document.querySelectorAll(`.${_cookie}`).forEach((i) => {
      i.click();
      e.preventDefault();
    });
  };
}
fontSize();
</script>
