# Images / 圖片及多媒體設定

?>檔案名稱：sass / element /`image.scss`

---

圖片在網頁上需要設定的細節非常多，HyUI 提供以下快速設定：

## 圖片形狀

直接在`img`加上所需要的`class`立即產生效果

<!-- panels:start -->
<section class="pic_list"> 
     <div class="col">
        <div class="imgContainer">
             <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/11.jpg" alt=""   class="lazy loaded cover" src="https://hywebu00.github.io/hyui_flex/images/demo/11.jpg" data-was-processed="true">
        </div>
        <h3>無class</h3>
      </div>
      <div class="col">
        <div class="imgContainer">
             <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/11.jpg" alt=""   class="lazy imgCircle loaded cover" src="https://hywebu00.github.io/hyui_flex/images/demo/11.jpg" data-was-processed="true">
        </div>
        <h3>class="imgCircle"</h3>
      </div>
      <div class="col">
        <div class="imgContainer">
             <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/11.jpg" alt=""   class="lazy imgRounded loaded cover" src="https://hywebu00.github.io/hyui_flex/images/demo/11.jpg" data-was-processed="true">
        </div>
        <h3>class="imgRounded"</h3>
      </div>
</section>
<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
<img src="..." />
<img src="..." class="imgCircle" />
<img src="..." class="imgRounded" /> //可用變數控制導角數值
```

<!-- tabs:end -->
<!-- <iframe height="450" style="width: 100%;" scrolling="no" title="" src="https://codepen.io/u00hyui/embed/RwVwqmy?defaultTab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/RwVwqmy">
  </a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe> -->

---

## 設定圖片外框比例

在單圖的部分也可在 SASS 設定比例，`任何比例`都可以，`1:1`、`4:3`、`16:9`為常見比例，設定方法請在`img`父層標籤設定`@include aspectRatio(寬度值,高度值)`即可，如以下範例：

<!-- panels:start-->
<div class="single_setting">
  <div class="thumbnail">
    <div class="imgContainer"><img data-src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon.png" alt="" class="lazy loaded" src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon.png" data-was-processed="true">
    </div>
    <h3>1:1</h3>
  </div>
  <div class="thumbnail">
    <div class="imgContainer">
      <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon.png" alt="" class="lazy loaded" src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon.png" data-was-processed="true">
    </div>
    <h3>4:3</h3>
  </div>
  <div class="thumbnail">
    <div class="imgContainer"><img data-src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon.png" alt="" class="lazy loaded" src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon.png" data-was-processed="true">
    </div>
    <h3>16:9</h3>
  </div>
</div>
<!-- panels:end -->

<!-- tabs:start -->

#### **HTML**

```html
<div class="imgContainer1"><img src="..." alt="..." /></div>
<div class="imgContainer2"><img src="..." alt="..." /></div>
<div class="imgContainer3"><img src="..." alt="..." /></div>
```

#### **css**

```sass
.imgContainer1{
    @include aspectRatio(1,1);      //設定比例 1:1
}
.imgContainer2{
    @include aspectRatio(4,3);      //設定比例 4:3
}
.imgContainer3{
    @include aspectRatio(16,9);     //設定比例 16:9
}
```

<!-- tabs:end -->

<!-- <iframe height="430" style="width: 100%;" scrolling="no" title="設定圖片外框比例" src="https://codepen.io/u00hyui/embed/OJmJdam?defaultTab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/OJmJdam">
  設定圖片外框比例</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe> -->

---

## 設定圖片 object-fit 屬性

因外框已設定比例，但內含之圖片往往不盡然與外框比例相符，針對不同圖片呈現需求可於`img`標籤中設定不同的 classname 給予不同之圖片效果，包括`none`、`contain`、`fill`、`cover`，屬性與`object-fit`之 css 設定相同。

<!-- panels:start -->

<div class="single_setting">
  <div class="thumbnail">
    <div class="imgContainer"><img data-src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon.png" alt="" class="lazy loaded cover" src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon.png" data-was-processed="true">
    </div>
    <h3>1:1 (object-fit:cover)</h3>
  </div>
  <div class="thumbnail">
    <div class="imgContainer">
      <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon.png" alt="" class="lazy loaded cover" src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon.png" data-was-processed="true">
    </div>
    <h3>4:3 (object-fit:cover)</h3>
  </div>
  <div class="thumbnail">
    <div class="imgContainer"><img data-src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon.png" alt="" class="lazy loaded cover" src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon.png" data-was-processed="true">
    </div>
    <h3>16:9 (object-fit:cover)</h3>
  </div>
</div>

<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
<div class="imgContainer1"><img src="..." alt="..." class="cover" /></div>
<div class="imgContainer2"><img src="..." alt="..." class="cover" /></div>
<div class="imgContainer3"><img src="..." alt="..." class="cover" /></div>
```

<!-- tabs:end -->

<!-- <iframe height="430" style="width: 100%;" scrolling="no" title="設定圖片object-fit屬性" src="https://codepen.io/u00hyui/embed/BaRabLY?defaultTab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/BaRabLY">
  設定圖片object-fit屬性</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe> -->

### 嵌入 iframe 的結構完全如上述圖片設定

<!-- <iframe height="430" style="width: 100%;" scrolling="no" title="嵌入iframe的結構" src="https://codepen.io/u00hyui/embed/MWmWxmd?defaultTab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/MWmWxmd">
  嵌入iframe的結構</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe> -->

<!-- panels:start -->
<div class="single_setting">
  <div class="thumbnail">
    <div class="imgContainer"><iframe src="https://www.youtube.com/embed/FxyrmBOiSqg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>
    </div>
    <h3>1:1</h3>
  </div>
  <div class="thumbnail">
    <div class="imgContainer">
      <iframe src="https://www.youtube.com/embed/FxyrmBOiSqg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>
    </div>
    <h3>4:3</h3>
  </div>
  <div class="thumbnail">
    <div class="imgContainer"><iframe src="https://www.youtube.com/embed/FxyrmBOiSqg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>
    </div>
    <h3>16:9</h3>
  </div>
</div>
<!-- panels:end -->

<!-- tabs:start -->

#### **HTML**

```html
<div class="imgContainer1"><iframe src="..."></iframe></div>
<div class="imgContainer2"><iframe src="..."></iframe></div>
<div class="imgContainer3"><iframe src="..."></iframe></div>
```

<!-- tabs:end -->

### 不同 object-fit 效果

圖片比例，以 object-fit css 做設定

<!-- panels:start -->
<section class="pic_list">
  <div class="col">
    <div class="imgContainer">
      <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon1.png" alt="" class="lazy loaded none" src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon1.png" data-was-processed="true">
    </div>
    <h3>none</h3>
  </div>
  <div class="col">
    <div class="imgContainer">
      <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon1.png" alt="" class="lazy loaded contain" src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon1.png" data-was-processed="true">
    </div>
    <h3>contain</h3>
  </div>
  <div class="col">
    <div class="imgContainer">
      <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon1.png" alt="" class="lazy loaded fill" src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon1.png" data-was-processed="true">
    </div>
    <h3>fill</h3>
  </div>
  <div class="col">
    <div class="imgContainer">
      <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon1.png" alt="" class="lazy loaded cover" src="https://hywebu00.github.io/hyui_flex/images/demo/doraemon1.png" data-was-processed="true">
    </div>
    <h3>cover</h3>
  </div>
</section>
<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
<div class="imgContainer"><img src="..." class="none" /></div>
<div class="imgContainer"><img src="..." class="contain" /></div>
<div class="imgContainer"><img src="..." class="fill" /></div>
<div class="imgContainer"><img src="..." class="cover" /></div>
```

<!-- tabs:end -->

<!-- <iframe height="360" style="width: 100%;" scrolling="no" title="不同object-fit效果" src="https://codepen.io/u00hyui/embed/LYyYazR?defaultTab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/LYyYazR">
  不同object-fit效果</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe> -->

## 使用 Lazyload 延遲載入

<iframe height="650" style="width: 100%;" scrolling="no" title="圖片形狀" src="https://codepen.io/u00hyui/embed/gOWOyLZ?defaultTab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/gOWOyLZ">
  圖片形狀</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

<!-- panels:start -->
<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
<div class="imgContainer">
  <img data-src="..." alt="圖片說明" class="lazy" />
  <noscript><img src="..." /></noscript>
  <!-- 關閉js無障礙用-->
</div>
```

<!-- tabs:end -->

:::warning
請注意 :warning: slick 套件本身有 lazyload 設定，請參考 [slider.htm](/Rd3leLQ0S3KGfHlJ3oS8ag)
:::

## JQuery 設定:round_pushpin:

頁面如有<span class="focus3">img</span>class 有設定<span class="focus3">lazy</span>皆會套用 lazyload 的效果。

```javascript
/*-----------------------------------*/
////////////// lazy load //////////////
/*-----------------------------------*/
if ($('img.lazy').length > 0) {
  $('img.lazy').show().lazyload({
    placeholder: 'images/basic/placeholder.gif',
    effect: 'fadeIn',
    fadeTime: 600,
  });
}
```

---

## Picturefill 搭配 Lazyload

<iframe height="380" style="width: 100%;" scrolling="no" title="" src="https://codepen.io/u00hyui/embed/ExmxJow?defaultTab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/ExmxJow">
  </a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### 建議縮圖標準

<table>
    <thead>
        <tr>
            <th>media尺寸</th>
            <th>圖片建議寬度尺寸</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>source media="(min-width: 1200px)</td>
            <td><span style="color:red">1960</span></td>
        </tr>
        <tr>
            <td>source media="(min-width: 992px)</td>
            <td><span style="color:red">1200</span></td>
        </tr>
        <tr>
            <td>source media="(min-width: 576px)</td>
            <td><span style="color:red">900</span></td>
        </tr>
        <tr>
            <td>source media="(max-width: 575px)</td>
            <td><span style="color:red">600</span></td>
        </tr>
    </tbody>
</table>

```html=
<picture>
    <source media="(min-width: 1200px)" srcset="images/demo/01.jpg">
    <source media="(min-width: 992px)" srcset="images/demo/02.jpg">
    <source media="(min-width: 576px)" srcset="images/demo/03.jpg">
    <source media="(max-width: 575px)" srcset="images/demo/04.jpg">
    <img data-src="images/demo/01.jpg" class="lazy">
    <noscript><img src="images/demo/01.jpg"></noscript>
    <!-- img都以最大圖為標準 -->
</picture>
```

:::warning
請注意 :warning:

- noscript 為必要加上的設定，因為 data-src 和 data-oringinal 並沒有把 src 路徑顯示，圖會出不來。
- 請先跟工程師確認能否產生縮圖以及確定斷點。
  :::

<span class="focus3">sourece media</span>的部分可調整斷點數值，目前是使用 hyUI 預設的[斷點](https://)，<span class="focus3">srcset</span>在製作時可用[https://placeholder.com/](https://placeholder.com/) 產生最佳的圖像大小。 特別注意的是：在不支援<span class="focus3">picture</span>或是關閉無障礙時，<span class="focus3">img</span>的<span class="focus3">data-src</span>以及<span class="focus3">noscript</span>的<span class="focus3">src</span>都帶入最大尺寸的圖像尤佳。

### 範例：

```html=
<picture>
    <source media="(min-width: 1200px)" srcset="大尺寸">
    <source media="(min-width: 992px)" srcset="中尺寸">
    <source media="(min-width: 576px)" srcset="小尺寸">
    <source media="(max-width: 575px)" srcset="超小尺寸">
    <img data-src="大尺寸" class="lazy">
    <noscript><img src="大尺寸"></noscript>
</picture>
```

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />

<style>
/* 顏色設定 <span class="blue"></span>*/
.pic_list {
  display: flex;
  flex-wrap: wrap;
  text-align: left;
  overflow: hidden;
}
.pic_list .col {
  width: calc(100% * 0.33333);
  flex-basis: calc(100% * 0.33333);
  padding: 1em;
}
@media screen and (max-width: 991px) {
  .pic_list .col {
    width: 100%;
    flex-basis: 100%;
  }
}
.pic_list h3 {
  color: #000;
  text-align: center;
  font-size: 1.25em;
  margin-top: 0.25em;
}
.pic_list .imgContainer {
  width: 100%;
  overflow: hidden;
  background: transparent;

}
.pic_list .imgContainer:before {
  display: inline-block;
  content: "";
  padding-top: 100%;
}

/* 設定圖片外匡比例 start */
.single_setting {
  display: flex;
  flex-wrap: wrap;
  text-align: left;
  overflow: hidden;
  padding: 1em;
  align-items: flex-start;
}
.single_setting .thumbnail {
  width: calc(100% * 0.33333 - 2em);
  flex-basis: calc(100% * 0.33333 - 2em);
  margin: 1em;
}
@media screen and (max-width: 575px) {
  .single_setting .thumbnail {
    width: 100%;
    flex-basis: 100%;
  }
}
.single_setting .thumbnail:nth-child(1) .imgContainer:before {
  padding-top: 100%;
}
.single_setting .thumbnail:nth-child(2) .imgContainer:before {
  padding-top: calc(3 / 4 * 100%);
}
.single_setting .thumbnail:nth-child(3) .imgContainer:before {
  padding-top: calc(9 / 16 * 100%);
}
.single_setting h3 {
  color: #000;
  text-align: center;
}
.single_setting .imgContainer {
  width: 100%;
  overflow: hidden;
  background: #f1f1f1;
}
.single_setting .imgContainer:before {
  display: inline-block;
  content: "";
}
.single_setting .imgContainer img {
  display: block;
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  width: 100%;
  height: 100%;
  margin: auto;
}
/* 設定圖片外匡比例 end */
/* 設定圖片 object-fit 屬性 start */
.single_setting {
  display: flex;
  flex-wrap: wrap;
  text-align: left;
  overflow: hidden;
  padding: 1em;
  align-items: flex-start;
}
.single_setting .thumbnail {
  width: calc(100% * 0.33333 - 2em);
  flex-basis: calc(100% * 0.33333 - 2em);
  margin: 1em;
}
@media screen and (max-width: 575px) {
  .single_setting .thumbnail {
    width: 100%;
    flex-basis: 100%;
  }
}
.single_setting .thumbnail:nth-child(1) .imgContainer:before {
  padding-top: 100%;
}
.single_setting .thumbnail:nth-child(2) .imgContainer:before {
  padding-top: calc(3 / 4 * 100%);
}
.single_setting .thumbnail:nth-child(3) .imgContainer:before {
  padding-top: calc(9 / 16 * 100%);
}
.single_setting h3 {
  color: #000;
  text-align: center;
}
.single_setting .imgContainer {
  width: 100%;
  overflow: hidden;
  background: #f1f1f1;
}
.single_setting .imgContainer:before {
  display: inline-block;
  content: "";
}
.single_setting .imgContainer img {
  display: block;
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  width: 100%;
  height: 100%;
  margin: auto;
}
/* 設定圖片 object-fit 屬性 end */

/* 嵌入 iframe 的結構完全如上述圖片設定start */
.single_setting {
  display: flex;
  flex-wrap: wrap;
  text-align: left;
  overflow: hidden;
  padding: 1em;
  align-items: flex-start;
}
.single_setting .thumbnail {
  width: calc(100% * 0.33333 - 2em);
  flex-basis: calc(100% * 0.33333 - 2em);
  margin: 1em;
}
@media screen and (max-width: 575px) {
  .single_setting .thumbnail {
    width: 100%;
    flex-basis: 100%;
  }
}
.single_setting .thumbnail:nth-child(1) .imgContainer:before {
  padding-top: 100%;
}
.single_setting .thumbnail:nth-child(2) .imgContainer:before {
  padding-top: calc(3 / 4 * 100%);
}
.single_setting .thumbnail:nth-child(3) .imgContainer:before {
  padding-top: calc(9 / 16 * 100%);
}
.single_setting h3 {
  color: #000;
  text-align: center;
}
.single_setting .imgContainer {
  width: 100%;
  overflow: hidden;
  background: #f1f1f1;
}
.single_setting .imgContainer:before {
  display: inline-block;
  content: "";
}
.single_setting .imgContainer img {
  display: block;
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  width: 100%;
  height: 100%;
  margin: auto;
}
/* 嵌入 iframe 的結構完全如上述圖片設定end */

/* 不同 object-fit 效果 start */
.pic_list {
  display: flex;
  flex-wrap: wrap;
  text-align: left;
  overflow: hidden;
}
.pic_list .col {
  width: 25%;
  flex-basis: 25%;
  padding: 1em;
}
@media screen and (max-width: 575px) {
  .pic_list .col {
    width: 100%;
    flex-basis: 100%;
  }
}
.pic_list h3 {
  color: #000;
  text-align: center;
}
.pic_list .imgContainer {
  width: 100%;
  overflow: hidden;
  background: #f1f1f1;
}
.pic_list .imgContainer:before {
  display: inline-block;
  content: "";
  padding-top: 100%;
}

/* 不同 object-fit 效果 end */

</style>
