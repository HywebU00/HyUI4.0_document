# Notice / 提示訊息

?>檔案名稱：sass/ module / `notice.scss`

通常用於表單輸入狀態之提示，可自由替換提示訊息之文本。

<section class="demo">
<div class="notice">這是一般提醒訊息區塊</div>
<div class="noticeInfo">這是一般提醒訊息區塊</div>
<div class="noticeSuccess">您已經成功登入</div>
<div class="noticeWarning">這似乎不是一個正常的Email格式</div>
<div class="noticeError">您輸入的帳號密碼有誤！</div>
</section>

## 預設提示訊息

<!-- tabs:start -->

#### **HTML**

```html
<div class="notice">這是一般提醒訊息區塊</div>
<div class="noticeInfo">這是一般提醒訊息區塊</div>
<div class="noticeSuccess">您已經成功登入</div>
<div class="noticeWarning">這似乎不是一個正常的Email格式</div>
<div class="noticeError">您輸入的帳號密碼有誤！</div>
```

<!-- tabs:end -->

<!-- <iframe height="290" style="width: 100%;" scrolling="no" title="Notice / 提示訊息" src="https://codepen.io/u00hyui/embed/rNyxZdv?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/rNyxZdv'>Notice / 提示訊息</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe> -->

## 有按鈕的提示訊息

<section class="demo">
<div class="notice">這是一般提醒訊息區塊 <a href="#" class="close"><img src="https://raw.githubusercontent.com/HywebU00/HyUI_v4.0/f4c5bef45e00de3d367ac27c2484d7ca1c5a49d8/images/basic/icon_close.svg" alt=""></a>
</div>
<div class="noticeInfo">這是一般提醒訊息區塊 <a href="#" class="close"><img src="https://raw.githubusercontent.com/HywebU00/HyUI_v4.0/f4c5bef45e00de3d367ac27c2484d7ca1c5a49d8/images/basic/icon_close.svg" alt=""></a>
</div>
<div class="noticeSuccess">您已經成功登入 <a href="#" class="close"><img src="https://raw.githubusercontent.com/HywebU00/HyUI_v4.0/f4c5bef45e00de3d367ac27c2484d7ca1c5a49d8/images/basic/icon_close.svg" alt=""></a>
</div>
<div class="noticeWarning">這似乎不是一個正常的Email格式 <a href="#" class="close"><img src="https://raw.githubusercontent.com/HywebU00/HyUI_v4.0/f4c5bef45e00de3d367ac27c2484d7ca1c5a49d8/images/basic/icon_close.svg" alt=""></a>
</div>
<div class="noticeError">您輸入的帳號密碼有誤！ <a href="#" class="close"><img src="https://raw.githubusercontent.com/HywebU00/HyUI_v4.0/f4c5bef45e00de3d367ac27c2484d7ca1c5a49d8/images/basic/icon_close.svg" alt=""></a>
</div>
</section>
<!-- tabs:start -->

#### **HTML**

```html
<div class="notice">
  這是一般提醒訊息區塊 <a href="#" class="close"><img src="images/basic/icon_close.svg" alt="" /></a>
</div>
<div class="noticeInfo">
  這是一般提醒訊息區塊 <a href="#" class="close"><img src="images/basic/icon_close.svg" alt="" /></a>
</div>
<div class="noticeSuccess">
  您已經成功登入 <a href="#" class="close"><img src="images/basic/icon_close.svg" alt="" /></a>
</div>
<div class="noticeWarning">
  這似乎不是一個正常的Email格式 <a href="#" class="close"><img src="images/basic/icon_close.svg" alt="" /></a>
</div>
<div class="noticeError">
  您輸入的帳號密碼有誤！ <a href="#" class="close"><img src="images/basic/icon_close.svg" alt="" /></a>
</div>
```

#### **JavaScript**

```javascript
document.querySelectorAll('[class*="notice"] a.close').forEach((i) => {
  i.addEventListener('click', (e) => {
    i.parentNode.style.display = 'none';
    e.preventDefault();
  });
});
```

<!-- tabs:end -->

<!-- <iframe height="290" style="width: 100%;" scrolling="no" title="Notice / 提示訊息- 有關閉按鈕" src="https://codepen.io/u00hyui/embed/wvJMEXz?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/wvJMEXz'>Notice / 提示訊息- 有關閉按鈕</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe> -->

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<style>
  .demo{
    margin:4em 0;
  }
</style>
<script>
  document.querySelectorAll('[class*="notice"] a.close').forEach((i) => {
  i.addEventListener('click', (e) => {
    i.parentNode.style.display = 'none';
    e.preventDefault();
  });
});
</script>
