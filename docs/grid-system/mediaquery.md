# Mediaquery

## 選擇優雅降級(Graceful Degradation)的開發流程

?> 目前大部分的網站規格是以 IE9+、FireFox、Chrome 以及 Safari 為主流瀏覽器，且 UI 設計師產出之 mockup 大部分以 PC 版本作為風格確認，因此先以主流瀏覽器為測試對象，再往下兼容行動版以及各種不同瀏覽器的呈現。

![](https://i.imgur.com/7de2I7B.jpg)

### 如何自訂自己的斷點

可在`variable.scss`自訂斷點，預設是以 `1400px`、`992px`、 `768px` 、 `576px` 為分界

```sass
//mediaquery breakpoint
$screenLg:        1400px !default;        //電腦
$screenMd:        992px  !default;        //平板
$screenSm:        768px  !default;        //手機
$screenXs:        576px  !default;        //極小尺寸
```

### SCSS 設定 max

針對不同的瀏覽器寬度斷點設定，HyUI 提供快速套用變數的 `mixin` ，供開發者直覺地且輕易地在樣式表分別寫出不同的效果

!>請注意順序，如果是使用 HyUI 預設斷點 mixin 是由較寬螢幕至最小寬度依序設定，避免被覆蓋。

```sass
.wrapper {
  margin: 0 auto;
  width: 100%;
  @include screen('notebook') {
      width: 85%; }
  @include screen('tablet') {
      width: 55%; }
  @include screen('mobile') {
      width: 85%; }
  @include screen('xsMobile') {
      width: 85%; }
}
```

CSS 輸出

```sass
.wrapper {
    margin: 0 auto;
    width: 100%; }
@media screen and (max-width: 1399px) {
    .wrapper {width: 85%; } }
@media screen and (max-width: 991px) {
    .wrapper {width: 55%; } }
@media screen and (max-width: 767px) {
    .wrapper {width: 85%; } }
@media screen and (max-width: 575px) {
    .wrapper {width: 85%; } }
```

### SCSS 設定 min

```sass
.wrapper {
  margin: 0 auto;
  width: 100%;
  @include screen('desktop') {
      width: 90%; }
  @include screen('tabletMin') {
      width: 55%; }
  @include screen('mobileMin') {
      width: 85%; }
  @include screen('xsMobileMin') {
      width: 85%; }
}
```

CSS 輸出

```sass
.wrapper {
    margin: 0 auto;
    width: 100%; }
@media screen and (min-width: 1400px) {
    .wrapper {width: 90%; } }
@media screen and (min-width: 991px) {
    .wrapper {width: 55%; } }
@media screen and (min-width: 767px) {
    .wrapper {width: 85%; } }
@media screen and (min-width: 575px) {
    .wrapper {width: 85%; } }
```

<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>
