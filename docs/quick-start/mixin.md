# mixin / extend 引用列表

## extend

?> 原始設定：../sass/common/mixins/`extend.scss`

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

?> 原始設定：../sass/common/mixins/`mediaquery.scss`

```sass
@include screen('desktop'){}            // min-width: 1400px
@include screen('notebook'){}           // max-width: 1399px
@include screen('tablet'){}             // max-width: 991px
@include screen('mobile'){}             // max-width: 767px
@include screen('xsMobile'){}          // max-width: 575px
```

### 格線系統

#### bootstrap 格線系統

?> 原始設定：：../sass/common/mixins/`bootstrapGrid.scss`

```sass
.col{
    @include make-xs-column(12);              // xs_mobile
    @include make-sm-column(6);               // mobile
    @include make-md-column(3);               // tablet
    @include make-lg-column(3);               // desktop
    @include gutter();                        // 容器內距 padding
}
```

#### flex 格線系統

?> 原始設定：../sass/common/mixins/`flex-grid.scss`

使用 flex 分割欄位，有兩種分割方式：<br>

- 均分：每欄 <b >欄寬都相同</b><br>
- 自由分配：每欄 <b >欄寬不相同，加總等於 12</b>。

[『均分』、『自由分配』的算式原理](https://hackmd.io/@lizewu/r1eU6MPBw)

```sass
// step 0、設定 flex 的 margin gutter
$m-gutter: 4px;

// 均分 equal
.papa{
    // step 1、父層設定：
    // 1. display: flex;
    // 2. flex-flow: row wrap;
    // 3. justify-content: space-between;
    @extend %flex_set;

    // step 2、子層設定：欄數、margin gutter
    // margin、padding，務必加上『單位』才能計算！
    .col{
        @include flex-xs-equal(1, 0px);
        @include flex-sm-equal(2, $m-gutter);
        @include flex-md-equal(2, $m-gutter);
        @include flex-lg-equal(2, $m-gutter);
        @include gutter();
    }
}

// 自由搭配
.flex_8_4{
    @extend %flex_set;
    .col{
        @include flex-xs(12, 0px);
        @include flex-sm(6, $m-gutter);
        @include flex-md(8, $m-gutter);
        @include flex-lg(8, $m-gutter);
        @include gutter();

        &:nth-child(2){
            @include flex-xs(12, 0px);
            @include flex-sm(6, $m-gutter);
            @include flex-md(4, $m-gutter);
            @include flex-lg(4, $m-gutter);
        }
    }
}

```

### 漸層

?> 原始設定：：../sass/common/mixins/`gradient.scss`

```sass
@include gradient(#07c, #06f, vertical);      // 水平
@include gradient(#07c, #06f, horizontal);    // 垂直
@include gradient(#07c, #06f, diagonal);      // 對角線
@include gradient(#07c, #06f, circle);        // 圓形
```

### 文字刪節號

?> 原始設定：：../sass/common/mixins/`text-overflow.scss`

```sass
@include text-overflow;                        // 單行
@include text-line(2,23px);                    // 多行（行數、行高）
```

### 清除 li 格式

?> 原始設定：：../sass/common/mixins/`li-reset.scss`

```sass
@include li-reset;                            // 清除li預設
@include img-responsive;                      // 圖片
```

### 圖片比例

?> 原始設定：../sass/common/mixins/`image.scss`

```sass
@include aspect-ratio(4,3);                   // 圖片比例，4:3
```

<h4>附加說明</h4>

> 上述檔案，全部引用至../sass/common/`mixin.scss`

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
