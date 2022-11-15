# Function / 回上一頁、友善列印、轉寄友人

?>檔案名稱：sass/ module /`function_panel.scss`

## 預設按鈕設定

<!-- function功能區塊 -->
<div class="function">
  <ul>
    <li><a href="javascript:history.back()">回上一頁</a></li>
    <li><a href="javascript:;">友善列印</a></li>
    <li><a href="javascript:;">轉寄友人</a></li>
  </ul>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="function">
  <ul>
    <li><a href="javascript:history.back()">回上一頁</a></li>
    <li><a href="#">友善列印</a></li>
    <li><a href="#">轉寄友人</a></li>
  </ul>
</div>
```

<!-- tabs:end -->

<!-- <iframe height="300" style="width: 100%;" scrolling="no" title="functionFunction /功能選單" src="https://codepen.io/u00hyui/embed/JjWjOde?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/JjWjOde">
  functionFunction /功能選單</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe> -->

## 有 icon 的按鈕設定

<div class="function">
  <ul>
    <li class="icon_back"><a href="javascript:;">回上一頁</a></li>
    <li class="icon_print"><a href="javascript:;">友善列印</a></li>
    <li class="icon_forward"><a href="javascript:;">轉寄友人</a></li>
  </ul>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="function">
  <ul>
    <li class="icon_back"><a href="#">回上一頁</a></li>
    <li class="icon_print"><a href="#">友善列印</a></li>
    <li class="icon_forward"><a href="#">轉寄友人</a></li>
  </ul>
</div>
```

<!-- tabs:end -->

<!-- <iframe height="300" style="width: 100%;" scrolling="no" title="functionFunction /功能選單   有icon" src="https://codepen.io/u00hyui/embed/oNZNobV?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/oNZNobV">
  functionFunction /功能選單   有icon</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe> -->

## 加入 functionPanel 的按鈕設定

<div class="functionPanel">
  <!-- function功能區塊 -->
  <div class="function">
    <ul>
      <li class="back"><a href="javascript:history.back()">回上一頁</a></li>
      <li class="print"><a href="javascript:;">友善列印</a></li>
      <li class="forward"><a href="javascript:;">轉寄友人</a></li>
    </ul>
  </div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="functionPanel">
  <!-- function功能區塊 -->
  <div class="function">
    <ul>
      <li class="back"><a href="javascript:history.back()">回上一頁</a></li>
      <li class="print"><a href="javascript:;">友善列印</a></li>
      <li class="forward"><a href="javascript:;">轉寄友人</a></li>
    </ul>
  </div>
</div>
```

<!-- tabs:end -->

<!-- <iframe height="300" style="width: 100%;" scrolling="no" title="Function/功能選單- 加入function_panel內" src="https://codepen.io/u00hyui/embed/YzZzEZK?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/YzZzEZK">
  Function/功能選單- 加入function_panel內</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe> -->

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<style>
   .function{
    margin:4em 0 ;
   }
  .function a{
    color:#fff;
  }
</style>
