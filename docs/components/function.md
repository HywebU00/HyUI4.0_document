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

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<style>
   .function{
    margin:4em 0 ;
   }
  .function a{
    color:#fff;
  }
</style>
