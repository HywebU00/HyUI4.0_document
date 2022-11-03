# Images / 圖片及多媒體設定

:::warning
檔案名稱：sass / element / <span class="focus2">\_image.scss</span>
:::

1. **<span class="focus">[圖片形狀](#item-1):arrow_down:</span>**
2. **<span class="focus">[設定圖片外框比例](#item-2):arrow_down:</span>**
3. **<span class="focus">[設定圖片 object-fit 屬性](#item-3):arrow_down:</span>**
4. **<span class="focus">[使用 Lazyload 延遲載入](#item-4):arrow_down:</span>**
5. **<span class="focus">[Picturefill 搭配 Lazyload](#item-5):arrow_down:</span>**

---

圖片在網頁上需要設定的細節非常多，HyUI 提供以下快速設定：

## <span style="font-size:2em;margin-right:.2em;color:#21BAFF;" id="item-1">01. </span>圖片形狀

直接在<span class="focus3">img</span>加上所需要的<span class="focus3">class</span>立即產生效果

<iframe height="450" style="width: 100%;" scrolling="no" title="" src="https://codepen.io/u00hyui/embed/RwVwqmy?defaultTab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/RwVwqmy">
  </a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

```html=
<img src="..." >
<img src="..." class="img_circle">
<img src="..." class="img_rounded">          //可用變數控制導角數值
```

---

## <span style="font-size:2em;margin-right:.2em;color:#21BAFF;" id="item-2">02. </span>設定圖片外框比例

在單圖的部分也可在 SASS 設定比例，<span class="focus3">任何比例</span>都可以，<span class="focus3">1:1</span>、<span class="focus3">4:3</span>、<span class="focus3">16:9</span> 為常見比例，設定方法請在<span class="focus3">img</span>父層標籤設定<span class="focus3">@include aspect-ratio(寬度值,高度值)</span>即可，如以下範例：

<iframe height="430" style="width: 100%;" scrolling="no" title="設定圖片外框比例" src="https://codepen.io/u00hyui/embed/OJmJdam?defaultTab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/OJmJdam">
  設定圖片外框比例</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

```html=
<div class="img-container1"><img src="..." alt="..."></div>
<div class="img-container2"><img src="..." alt="..."></div>
<div class="img-container3"><img src="..." alt="..."></div>
```

### SCSS 設定

```css=
.img-container1{
    @include aspect-ratio(1,1);      //設定比例 1:1
}
.img-container2{
    @include aspect-ratio(4,3);      //設定比例 4:3
}
.img-container3{
    @include aspect-ratio(16,9);     //設定比例 16:9
}
```

---

## <span style="font-size:2em;margin-right:.2em;color:#21BAFF;" id="item-3">03. </span>設定圖片 object-fit 屬性

因外框已設定比例，但內含之圖片往往不盡然與外框比例相符，針對不同圖片呈現需求可於<span class="focus3">img</span>標籤中設定不同的 classname 給予不同之圖片效果，包括<span class="focus3">none</span>、<span class="focus3">contain</span>、<span class="focus3">fill</span>、<span class="focus3">cover</span>，屬性與<span class="focus3">object-fit</span>之 css 設定相同。

<iframe height="430" style="width: 100%;" scrolling="no" title="設定圖片object-fit屬性" src="https://codepen.io/u00hyui/embed/BaRabLY?defaultTab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/BaRabLY">
  設定圖片object-fit屬性</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

```html=
<div class="img-container1"><img src="..." alt="..." class="cover"></div>
<div class="img-container2"><img src="..." alt="..." class="cover"></div>
<div class="img-container3"><img src="..." alt="..." class="cover"></div>
```

### 嵌入 iframe 的結構完全如上述圖片設定

<iframe height="430" style="width: 100%;" scrolling="no" title="嵌入iframe的結構" src="https://codepen.io/u00hyui/embed/MWmWxmd?defaultTab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/MWmWxmd">
  嵌入iframe的結構</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

```html=
<div class="img-container1"><iframe src="..."></iframe></div>
<div class="img-container2"><iframe src="..."></iframe></div>
<div class="img-container3"><iframe src="..."></iframe></div>
```

### 不同 object-fit 效果

<iframe height="360" style="width: 100%;" scrolling="no" title="不同object-fit效果" src="https://codepen.io/u00hyui/embed/LYyYazR?defaultTab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/LYyYazR">
  不同object-fit效果</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### 圖片比例，以 object-fit css 做設定

```html=
<div class="img-container"><img src="..." class="none" ></div>
<div class="img-container"><img src="..." class="contain" ></div>
<div class="img-container"><img src="..." class="fill" ></div>
<div class="img-container"><img src="..." class="cover" ></div>
```

## JQuery 設定:round_pushpin:

```javascript
/*--------------------------------------------------------*/
/////設定img 在IE9+ SAFARI FIREFOX CHROME 可以object-fit/////
/*--------------------------------------------------------*/
var userAgent, ieReg, ie;
userAgent = window.navigator.userAgent;
ieReg = /msie|Trident.*rv[ :]*11\./gi;
ie = ieReg.test(userAgent);
if (ie) {
  $('.img-container').each(function () {
    var imgUrl = $(this).find('img').attr('data-src');
    var $container = $(this);
    $container.has('.none').addClass('ie-object-none');
    $container.has('.none').css('backgroundImage', 'url(' + imgUrl + ')');
    $container.has('.cover').addClass('ie-object-cover');
    $container.has('.cover').css('backgroundImage', 'url(' + imgUrl + ')');
    $container.has('.fill').addClass('ie-object-fill');
    $container.has('.fill').css('backgroundImage', 'url(' + imgUrl + ')');
    $container.has('.contain').addClass('ie-object-contain');
    $container.has('.contain').css('backgroundImage', 'url(' + imgUrl + ')');
  });
}
```

---

## <span style="font-size:2em;margin-right:.2em;color:#21BAFF;" id="item-4">04. </span>使用 Lazyload 延遲載入

<iframe height="650" style="width: 100%;" scrolling="no" title="圖片形狀" src="https://codepen.io/u00hyui/embed/gOWOyLZ?defaultTab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/gOWOyLZ">
  圖片形狀</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

```html=
<div class="img-container">
    <img data-src="..." alt="圖片說明" class="lazy">
    <noscript><img src="..."></noscript> <!-- 關閉js無障礙用-->
</div>
```

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

## <span style="font-size:2em;margin-right:.2em;color:#21BAFF;" id="item-5">05. </span>Picturefill 搭配 Lazyload

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

<style>
/* 顏色設定 <span class="blue"></span>*/

.title{
    font-size: 26px; color: #fff;
    background:#00469C; display:inline-block;
    padding: 10px 20px 10px 30px;
    border-radius: 4px;
}
.sub-title{ font-size: 20px; color: #00469C; }
.box{
    padding: 1em 2em;
    background:#f5f5f5;
    margin: 10px 0;
    border: solid 1px #aaa;
}

.focus { color: #B20050; }
.focus2 {
    color: #222; 
    border: solid 1px #c8c8c8;
    display: inline-block;
    padding: 2px 10px; margin: 0 4px;
    border-radius: 4px;
    background: #fff;
}
.focus3{
    display: inline-block;
    background: #f1f1f1;
    padding: 0.1em 0.8em;
    border: 1px solid #f1f1f1;
    margin: 0px 5px;
    line-height: 1.35em;
    border-radius: 4px;
    color: #B20050;
    margin-top: 2px;
    font-size: 15px;
    font-weight: bold;
}
.link{ font-size: 20px; color: #B20050;}
.ui-infobar{ max-width:95%; }
.markdown-body{ max-width:95%; }
</style>
