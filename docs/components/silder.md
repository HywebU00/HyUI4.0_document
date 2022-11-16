# swiper 圖片輪播

###### tags: `HyUI`

檔案名稱：vendor/swiper/swiper-bundle.min.css
檔案名稱：sass/modual/\_swiper

HyUI 使用 <font color="#009ee7">slick</font> 的輪播模組，目前 hyUI <font color="#EE428B">vendor</font> 內含 <font color="#EE428B">swiper</font> ，如需要最新版，請到 <font color="#009ee7">[swiper](https://swiperjs.com/)</font> 官網下載。<br/>
[中文版](https://www.swiper.com.cn/)

## 請在網頁中匯入 swiper 外掛

swiper 屬於外掛，故放在 <font color="#EE428B">vendor</font> 資料夾裡，包括所有的圖檔、js、css

## 匯入外掛 CSS

```html
<link rel="stylesheet" type="text/css" href="vendor/swiper/swiper-bundle.min.css" />
```

## 匯入 JS

```html
<script src="vendor/swiper/swiper-bundle.min.js"></script>
```

## swiper 的基本設定

使用設定以 swiper 官方文件為準。<br/>
swiper 功能非常多可自行到 [中文版 API](https://www.swiper.com.cn/api/index.html) 觀看

## <font color="#009ee7">01.大圖輪播範例</font>

本版本輪播圖檔可使用 <font color="#EE428B">obect-fit</font> 設定，故上稿內容不限尺寸，皆可正常呈現。

<div class="mpSlider">
  <div class="swiper">
    <div class="swiper-wrapper">
      <div class="swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg" class="swiper-lazy" alt="圖說1" />
          <span class="caption">圖說1</span>
        </a>
      </div>
      <div class="swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/02.jpg" class="swiper-lazy" alt="圖說2" />
          <span class="caption">圖說1</span>
        </a>
      </div>
      <div class="swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/03.jpg" class="swiper-lazy" alt="圖說3" />
          <span class="caption">圖說1</span>
        </a>
      </div>
    </div>
  </div>
  <div class="swiper-button-prev"></div>
  <div class="swiper-button-next"></div>
  <div class="swiper-pagination"></div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<!-- 圖片輪播 start -->
<div class="mpSlider">
  <div class="swiper">
    <div class="swiper-wrapper">
      <!-- 此區塊以下為一筆 -->
      <div class="swiper-slide">
        <a href="#" title="">
          <picture>
            <source media="(min-width: 1200px)" data-srcset="images/demo/01.jpg" />
            <source media="(min-width: 992px)" data-srcset="images/demo/01.jpg" />
            <source media="(min-width: 576px)" data-srcset="images/demo/01.jpg" />
            <source media="(max-width: 575px)" data-srcset="images/demo/01.jpg" />
            <img data-src="images/demo/01.jpg" class="cover swiper-lazy" alt="圖說1" />
            <noscript><img src="images/demo/01.jpg" alt="圖說1" /></noscript>
          </picture>
          <span class="caption">圖說1</span>
        </a>
      </div>
      <!-- 此區塊以上為一筆 -->
      。 。 。
    </div>
  </div>

  <!--操控物件可以隨意放，但注意設定要對應到-->
  <!--前一筆-->
  <div class="swiper-button-prev"></div>
  <!--下一筆-->
  <div class="swiper-button-next"></div>
  <!--圓點-->
  <div class="swiper-pagination"></div>
</div>
<!-- 圖片輪播 end -->
```

#### **CSS**

```css
.mpSlider {
  overflow: hidden;
}
.mpSlider .swiper-slide {
  position: relative;
  line-height: 0;
}
.mpSlider .swiper-slide span {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  display: block;
  text-align: center;
  color: #fff;
  padding: 10px;
  background: rgba(0, 0, 0, 0.8);
  line-height: 1;
}
.mpSlider .swiper-slide img {
  height: 100%;
  width: 100%;
  object-fit: contain;
}
```

#### **JAVASCRIPT**

```javascript
const mpSlider = new Swiper('.mpSlider .swiper', {
  slidesPerView: 1, //顯示張數
  navigation: {
    nextEl: '.mpSlider .swiper-button-next', //下一張class
    prevEl: '.mpSlider .swiper-button-prev', //前一張class
  },
  pagination: {
    //顯示圓點
    el: '.swiper-pagination', //圓點 class
    type: 'bullets', //樣式參考 https://www.swiper.com.cn/api/pagination/299.html
    clickable: true, //設定後圓點才可以點擊
  },
  autoplay: {
    //自動播放
    delay: 5000, //自動播放的間隔
  },
  loop: true, //無限輪播
  effect: 'fade', //淡入
  fadeEffect: {
    crossFade: true, //上一張淡出，false上一張不淡出，下一張疊在上方
  },
  lazy: true,
});
```

<!-- tabs:end -->

## <font color="#009ee7">02.廣告輪播範例</font>

<div class="adSlider">
  <div class="swiper">
    <div class="swiper-wrapper">
      <div class="swiper-slide">
        <a href="#" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_01.jpg" class="swiper-lazy" alt="圖說1" />
        </a>
      </div>
      <div class="swiper-slide">
        <a href="#" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_02.jpg" class="swiper-lazy" alt="圖說2" />
        </a>
      </div>
      <div class="swiper-slide">
        <a href="#" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_03.jpg" class="swiper-lazy" alt="圖說3" />
        </a>
      </div>
      <div class="swiper-slide">
        <a href="#" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_04.jpg" class="swiper-lazy" alt="圖說4" />
        </a>
      </div>
      <div class="swiper-slide">
        <a href="#" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_05.jpg" class="swiper-lazy" alt="圖說5" />
        </a>
      </div>
      <div class="swiper-slide">
        <a href="#" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_06.jpg" class="swiper-lazy" alt="圖說6" />
        </a>
      </div>
      <div class="swiper-slide">
        <a href="#" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_07.jpg" class="swiper-lazy" alt="圖說7" />
        </a>
      </div>
    </div>
  </div>
  <div class="swiper-button-prev"></div>
  <div class="swiper-button-next"></div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<!-- 廣告輪播   start -->
<div class="adSlider">
  <div class="swiper">
    <div class="swiper-wrapper">
      <!-- 此區塊以下為一筆 -->
      <div class="swiper-slide">
        <a href="#" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_01.jpg" class="cover" alt="圖說1" />
        </a>
      </div>
      <!-- 此區塊以上為一筆 -->
      。。。
    </div>
  </div>

  <!--操控物件可以隨意放，但注意設定要對應到-->
  <!--前一筆-->
  <div class="swiper-button-prev"></div>
  <!--下一筆-->
  <div class="swiper-button-next"></div>
</div>
<!-- 廣告輪播   end -->
```

### **css**

```css
.adSlider {
  overflow: hidden;
}
.adSlider {
  position: relative;
  line-height: 0;
}
.adSlider span {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  display: block;
  text-align: center;
  color: #fff;
  padding: 10px;
  background: rgba(0, 0, 0, 0.8);
  line-height: 1;
}
.adSlider .swiper-slide img {
  height: 100%;
  width: 100%;
  object-fit: contain;
}
.adSlider .swiper-slide {
  height: 55px;
}
```

#### **JAVASCRIPT**

```javascript
const adSlider = new Swiper('.adSlider .swiper', {
  slidesPerView: 5, //顯示張數
  navigation: {
    nextEl: '.adSlider .swiper-button-next', //下一張class
    prevEl: '.adSlider .swiper-button-prev', //前一張class
  },
  loop: true, //無限輪播
  lazy: true, // lazy load
  preloadImages: false, // 多筆設定lazy時須設定
  centeredSlides: false, // 多筆設定lazy時須設定
  watchSlidesVisibility: true, // 多筆設定lazy時須設定
});
```

<!-- tabs:end -->

## <font color="#009ee7">03.照片輪播範例</font>

<div class="syncingSlider">
  <div class="swiper">
    <div class="swiper-wrapper">
      <div class="swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg" class="swiper-lazy" alt="圖說1" />
        </a>
      </div>
      <div class="swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/02.jpg" class="swiper-lazy" alt="圖說2" />
        </a>
      </div>
      <div class="swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/03.jpg" class="swiper-lazy" alt="圖說3" />
        </a>
      </div>
      <div class="swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/04.jpg" class="swiper-lazy" alt="圖說4" />
        </a>
      </div>
      <div class="swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/05.jpg" class="swiper-lazy" alt="圖說5" />
        </a>
      </div>
    </div>
  </div>
</div>

<div class="navSlider">
  <div class="swiper">
    <div class="swiper-wrapper">
      <div class="swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg" class="swiper-lazy" alt="圖說1" />
        </a>
      </div>
      <div class="swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/02.jpg" class="swiper-lazy" alt="圖說2" />
        </a>
      </div>
      <div class="swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/03.jpg" class="swiper-lazy" alt="圖說3" />
        </a>
      </div>
      <div class="swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/04.jpg" class="swiper-lazy" alt="圖說4" />
        </a>
      </div>
      <div class="swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/05.jpg" class="swiper-lazy" alt="圖說5" />
        </a>
      </div>
    </div>
  </div>
</div>

## HTML 範本

```html
<div class="Syncing_slider">
  <!--大圖slider-for-->
  <div class="Slider-for">
    <div>
      <div class="img-container">
        <img src="https://assets.imgix.net/examples/kingfisher.jpg?w=500&h=480&fit=crop&auto=format%2Cenhance&usm=20" />
      </div>
      <p>第一張圖說</p>
    </div>
    <div>
      <div class="img-container">
        <img src="https://assets.imgix.net/examples/puffins.jpg?w=800&h=480&fit=crop&auto=format%2Cenhance&usm=20" />
      </div>
      <p>第二張圖說</p>
    </div>
    <div>
      <div class="img-container">
        <img src="https://assets.imgix.net/examples/womanlandscape.jpg?w=800&h=480&fit=crop&auto=format%2Cenhance&usm=20" />
      </div>
      <p>第三張圖說</p>
    </div>
    <div>
      <div class="img-container">
        <img src="https://assets.imgix.net/unsplash/paperlamp.jpg?w=800&h=480&fit=crop&auto=format%2Cenhance&usm=20" />
      </div>
      <p>第四張圖說</p>
    </div>
  </div>
  <!-- slider-for end-->
  <div class="controls"></div>
  <!--小圖slider-nav-->
  <div class="Slider-nav">
    <div>
      <div class="img-container">
        <img src="https://assets.imgix.net/examples/kingfisher.jpg?w=800&h=480&fit=crop&auto=format%2Cenhance&usm=20" />
      </div>
      <p>第一張圖說</p>
    </div>
    <div>
      <div class="img-container">
        <img src="https://assets.imgix.net/examples/puffins.jpg?w=800&h=480&fit=crop&auto=format%2Cenhance&usm=20" />
      </div>
      <p>第二張圖說</p>
    </div>
    <div>
      <div class="img-container">
        <img src="https://assets.imgix.net/examples/womanlandscape.jpg?w=800&h=480&fit=crop&auto=format%2Cenhance&usm=20" />
      </div>
      <p>第三張圖說</p>
    </div>
    <div>
      <div class="img-container">
        <img src="https://assets.imgix.net/unsplash/paperlamp.jpg?w=800&h=480&fit=crop&auto=format%2Cenhance&usm=20" />
      </div>
      <p>第四張圖說</p>
    </div>
  </div>
  <!-- slider-nav end-->
</div>
```

## JQuery 設定:round_pushpin:

### 關於 slick 按鈕的 title 語系

因應無障礙需求，在左右箭頭需要有替代文字，但往往因為網站有不同語系需求，因此按鈕需要呈現不同語言的替代文字，例如:

<<font color="#009ee7">html</font> lang="<font color="#EE428B">zh-Hant</font>">中按鈕會呈現<<font color="#009ee7">button</font> class="slick-prev" ... title="<font color="#EE428B">前一則</font>">Previous</button>或是
<<font color="#009ee7">html</font> lang="<font color="#EE428B">en</font>" >中按鈕會呈現或是<<font color="#009ee7">button</font> class="<font color="#EE428B">slick-prev</font>" ... title="<font color="#EE428B">previous</font>">Previous</button>，
此時無法用同一種語言因應各種語系，HyUI 提供一組判斷語系之 javascript 設定，語系參照[W3C ISO Language Codes](https://www.w3schools.com/tags/ref_language_codes.asp)，可自行複製到各專案修改語系及對應之替代文字即可。注意：此程式並無預設放入 <font color="#EE428B">hyui.js</font>。

其中，程式是判斷語系字串中的前面字符作為判斷依據，目的是同一語系可能會有分支語系，但以開頭之語系英文字母做判斷。

## hyui.js 範例

```javascript
//不同語系
//無障礙切換slick箭頭語系
if ($('html')[0].hasAttribute('labg')) {
  var weblang = $('html').attr('lang');
  if (weblang.substring(0, 2) == 'zh') {
    $('.slick-prev').attr('title', '上一筆');
    $('.slick-next').attr('title', '下一筆');
  } else if (weblang.substring(0, 2) !== 'zh') {
    $('.slick-prev').attr('title', 'previous');
    $('.slick-next').attr('title', 'next');
  }
}
```

## 輪播項目之索引標籤(點點)提示

需補充較詳細之提示文字，讓使用導讀軟體之使用者可以明確了解該元件之功能與用途，目前以 <font color="#EE428B">單張輪播</font> 修改。

<font color="#009ee7">在所需 slider 做 js 調整</font>

```javascript
取文字
customPaging: function(slider, i) {
                var title = $(slider.$slides[i]).find('.title').html().trim();
                return $('<button type="button" aria-label="'+title+'"/>').text(title);
            }

取圖片的alt
customPaging: function(slider, i) {
             var title = $(slider.$slides[i]).find('img').attr('alt').trim();
            return $('<button type="button" aria-label="'+title+'"/>').text(title);
            }
```

<font color="#009ee7">slick.js 修改拿掉</font>

![](https://i.imgur.com/ABKdv6Z.jpg)

<font color="#009ee7">slick.min.js 修改拿掉</font>

![](https://i.imgur.com/gZlbY5u.jpg)

<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
.swiper-slide {
  position:relative;
  line-height:0;
}
.swiper-slide span{
  position:absolute;
  bottom:0;
  left:0;
  width:100%;
  display:block;
  text-align: center;
  color:#FFF;
  padding:10px;
  background:rgba(0,0,0,0.8);
  line-height:1;
}
.navSlider,
.mpSlider,
.adSlider{
  overflow:hidden;
}
.navSlider .swiper-slide img,
.mpSlider .swiper-slide img,
.adSlider .swiper-slide img{
  height:100%;
  width:100%;
  object-fit:contain;
}
.adSlider .swiper-slide{
  height:55px
}
.navSlider .swiper-slide{
  height:172px
}
</style>

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@8/swiper-bundle.min.css" />

<script>
const mpSlider = new Swiper('.mpSlider .swiper', {
  slidesPerView: 1, //顯示張數
  navigation: {
    nextEl: '.mpSlider .swiper-button-next', //下一張class
    prevEl: '.mpSlider .swiper-button-prev', //前一張class
  },
  pagination: {
    //顯示圓點
    el: '.mpSlider .swiper-pagination', //圓點 class
    type: 'bullets', //樣式參考 https://www.swiper.com.cn/api/pagination/299.html
    clickable :true,
  },
  autoplay: {
    //自動播放
    delay: 5000, //自動播放的間隔
  },
  loop: true, //無限輪播
  effect: 'fade', //淡入
  fadeEffect: {
    crossFade: true, //上一張淡出，false上一張不淡出，下一張疊在上方
  },
  lazy: true, //延遲載入
});

const adSlider = new Swiper('.adSlider .swiper', {
  slidesPerView: 5, //顯示張數
  navigation: {
    nextEl: '.adSlider .swiper-button-next', //下一張class
    prevEl: '.adSlider .swiper-button-prev', //前一張class
  },
  loop: true, //無限輪播
  lazy: true, // lazy load
  preloadImages: false, // 多筆設定lazy時須設定
  centeredSlides: false, // 多筆設定lazy時須設定
  watchSlidesVisibility: true, // 多筆設定lazy時須設定
});

const navSlider = new Swiper('.navSlider .swiper', {
  lazy: true, // lazy load
  preloadImages: false, // 多筆設定lazy時須設定
  centeredSlides: false, // 多筆設定lazy時須設定
  slidesPerView: 4,
  watchSlidesProgress: true,
});

const syncingSlider = new Swiper('.syncingSlider .swiper', {
  slidesPerView: 1, //顯示張數
  effect: 'fade', //淡入
  fadeEffect: {
    crossFade: true, //上一張淡出，false上一張不淡出，下一張疊在上方
  },
  lazy: true,
  thumbs: {
    swiper: navSlider,
  },
});
</script>
