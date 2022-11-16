# mixin / extend / function 引用列表

## extend

?> 原始設定：../sass/common/mixins/`_extend.scss`

```sass
// 繼承
@extend %slash;              // 斜線
@extend %arrowSetting;      // 箭頭
@extend %arrowDown;         // 箭頭：下
@extend %arrowRight;        // 箭頭：右
@extend %arrowUp;           // 箭頭：上
@extend %arrowLeft;         // 箭頭：左
@extend %flexSet;           // 啟動 display:flex
```

## mixin

### 瀏覽器斷點

?> 原始設定：../sass/common/mixins/`_mediaquery.scss`

```sass
//max-width
@include screen('notebook'){}         // max-width: 1399px
@include screen('tablet'){}           // max-width: 991px
@include screen('mobile'){}           // max-width: 767px
@include screen('xsMobile'){}         // max-width: 575px

//min-width
@include screen('desktop'){}          // min-width: 1400px
@include screen('tabletMin'){}        // min-width: 991px
@include screen('mobileMin'){}        // min-width: 767px
@include screen('xsMobileMin'){}      // min-width: 575px

//自訂
@include screenWidth('1200'){}        // max-width: 1200px
@include screenWidthMin('1200'){}        // min-width: 1200px
```

### 格線系統

#### bootstrap 格線系統

?> 原始設定：：../sass/common/mixins/`_bootstrapGrid.scss`

```sass
.col{
    @include makeXsColumn(12);              // xs_mobile
    @include makeXmColumn(6);               // mobile
    @include makeMdColumn(3);               // tablet
    @include makeLgColumn(3);               // desktop
    @include gutter();                        // 容器內距 padding
}
```

#### flex 格線系統

?> 原始設定：../sass/common/`_gridflex.scss`

使用 flex 分割欄位，有兩種分割方式：<br>

- 均分：每欄 <b >欄寬都相同</b><br>
- 自由分配：每欄 <b >欄寬不相同，加總等於 12</b>。

[『均分』、『自由分配』的算式原理](https://hackmd.io/@lizewu/r1eU6MPBw)

```sass
// step 0、設定 flex 的 margin gutter
$mGutter: 4px;

// 均分 equal
.papa{
    // step 1、父層設定：
    // 1. display: flex;
    // 2. flex-flow: row wrap;
    // 3. justify-content: space-between;
    @extend %flexSet;
    @include flexSet;

    // step 2、子層設定：欄數、margin gutter
    // margin、padding，務必加上『單位』才能計算！
    .col{
        @include flexXsEqual(1, 0px);
        @include flexSmEqual(2, $mGutter);
        @include flexMdEqual(2, $mGutter);
        @include flexLgEqual(2, $mGutter);
        @include gutter();
    }
}

// 自由搭配
.flex_8_4{
    @extend %flex_set;
    .col{
        @include flexXs(12, 0px);
        @include flexXm(6, $mGutter);
        @include flexMd(8, $mGutter);
        @include flexLg(8, $mGutter);
        @include gutter();

        &:nth-child(2){
          @include flexXs(12, 0px);
          @include flexXm(6, $mGutter);
          @include flexMd(4, $mGutter);
          @include flexLg(4, $mGutter);
        }
    }
}

```

### 漸層

?> 原始設定：../sass/common/mixins/`_gradient.scss`

```sass
@include gradient(#07c, #06f, vertical);      // 水平
@include gradient(#07c, #06f, horizontal);    // 垂直
@include gradient(#07c, #06f, diagonal);      // 對角線
@include gradient(#07c, #06f, circle);        // 圓形
```

### 文字刪節號

?> 原始設定：：../sass/common/mixins/`_text.scss`

```sass
@include textOverflow;                        // 單行
@include textLine(2,23px);                    // 多行（行數、行高）
```

### 清除 li 格式

?> 原始設定：：../sass/common/mixins/`_lireset.scss`

```sass
@include liReset;                            // 清除li預設
```

### 圖片比例

?> 原始設定：../sass/common/mixins/`_image.scss`

```sass
@include aspectRatio(4,3);                   // 圖片比例，4:3
```

### 文字大小轉換 px > rem

?> 原始設定：../sass/common/mixins/`_text.scss`

```sass
font-size:rem(16);                   // 文字大小，16px = 1rem
```

### 針對視覺隱藏，螢幕閱讀器會讀到

?> 原始設定：../sass/common/mixins/`_sronly.scss`

```sass
@include srOnly;                  // 無障礙螢幕閱讀器會讀到
```

?>**附加說明**<br>上述檔案，全部引用至../sass/`common` 資料夾內<br>

<style>
    .block-style{
  padding:2.2em 3em !important;
  background:#f8f8f8;
}
/* 顏色設定 <span class="blue"></span>*/
/* .title{
    font-size: 26px; color: #fff;
    background:#00469C; display:inline-block;
    padding: 10px 20px 10px 30px;
    border-radius: 4px;
}
.sub-title{ font-size: 20px; color: #00469C; }

.focus { color: #B20050; }
.focus2 {
    color: #222; border: solid 1px #c8c8c8;
    display: inline-block;
    padding: 2px 10px; margin: 0 4px;
    border-radius: 4px;
    background: #fff;
}
.link{ font-size: 20px; color: #B20050;}
.ui-infobar{ max-width:95%; }
.markdown-body{ max-width:95%; } */
</style>
