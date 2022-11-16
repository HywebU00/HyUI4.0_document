# swiper 圖片輪播

###### tags: `HyUI`

檔案名稱：vendor/swiper/swiper-bundle.min.css
檔案名稱：sass/ module /\_swiper

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

```javascript
const bannerSlider = new Swiper('.bannerSlider .swiper', {
  slidesPerView: 1, //顯示筆數
  spaceBetween: 20, //每筆之間的距離
  navigation: {
    nextEl: '.bannerSlider .nextSlider', //下一筆class，無障礙設定關係需要增加.nextSlider
    prevEl: '.bannerSlider .prevSlider', //前一筆class，無障礙設定關係需要增加.prevSlider
    disabledClass: 'swiperArrow-disabled', //不可點選樣式
  },
  pagination: {
    //顯示圓點
    el: '.swiperDots', //圓點 class
    type: 'bullets', //樣式參考 https://www.swiper.com.cn/api/pagination/299.html
    clickable: true, //設定後圓點才可以點擊
    renderBullet: function (index, className) {
      return '<span class="' + className + '">' + (index + 1) + '</span>';
    },
  },
  autoplay: {
    //自動播放
    delay: 5000, //自動播放的間隔
  },
  loop: true, //無限輪播
  effect: 'fade', //淡入
  fadeEffect: {
    crossFade: true, //上一筆淡出，false上一筆不淡出，下一筆疊在上方
  },
  lazy: true,
});
```

## <font color="#009ee7">01.大圖輪播範例</font>

本版本輪播圖檔可使用 <font color="#EE428B">obect-fit</font> 設定，故上稿內容不限尺寸，皆可正常呈現。

<div class="bannerSlider">
<div class="swiperBox">
  <div class="swiper">
    <div class="swiper-wrapper">
      <div class="imgContainer swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg" class="swiper-lazy" alt="圖說1" />
          <span class="caption">圖說</span>
        </a>
      </div>
      <div class="imgContainer swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/02.jpg" class="swiper-lazy" alt="圖說2" />
          <span class="caption">圖說2</span>
        </a>
      </div>
      <div class="imgContainer swiper-slide">
        <a href="javascript:;" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/03.jpg" class="swiper-lazy" alt="圖說3" />
          <span class="caption">圖說3</span>
        </a>
      </div>
    </div>
  </div>
  <div class="prevSlider swiperArrow"></div>
  <div class="nextSlider swiperArrow"></div>
  <div class="swiperDots"></div>
  </div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<!-- 圖片輪播 start -->
<div class="bannerSlider">
  <div class="swiperBox">
    <div class="swiper">
      <div class="swiper-wrapper">
        <!-- 此區塊以下為一筆 -->
        <div class="imgContainer swiper-slide">
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
    <div class="prevSlider swiperArrow"></div>
    <!--下一筆-->
    <div class="nextSlider swiperArrow"></div>
    <!--圓點-->
    <div class="swiperDots"></div>
  </div>
</div>
<!-- 圖片輪播 end -->
```

#### **CSS**

```css
.bannerSlider {
  position: relative;
}
```

#### **JAVASCRIPT**

```javascript
const bannerSlider = new Swiper('.bannerSlider .swiper', {
  slidesPerView: 1, //顯示張數
  navigation: {
    nextEl: '.bannerSlider .nextSlider.swiperArrow', //下一張class，無障礙設定關係需要增加.nextSlider
    prevEl: '.bannerSlider .prevSlider.swiperArrow', //前一張class，無障礙設定關係需要增加.prevSlider
  },
  pagination: {
    //顯示圓點
    el: '.swiperDots', //圓點 class
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
  <div class="swiperBox">
  <div class="swiper">
    <div class="swiper-wrapper">
      <div class="imgContainer swiper-slide">
        <a href="#" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_01.jpg" class="swiper-lazy" alt="圖說1" />
        </a>
      </div>
      <div class="imgContainer swiper-slide">
        <a href="#" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_02.jpg" class="swiper-lazy" alt="圖說2" />
        </a>
      </div>
      <div class="imgContainer swiper-slide">
        <a href="#" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_03.jpg" class="swiper-lazy" alt="圖說3" />
        </a>
      </div>
      <div class="imgContainer swiper-slide">
        <a href="#" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_04.jpg" class="swiper-lazy" alt="圖說4" />
        </a>
      </div>
      <div class="imgContainer swiper-slide">
        <a href="#" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_05.jpg" class="swiper-lazy" alt="圖說5" />
        </a>
      </div>
      <div class="imgContainer swiper-slide">
        <a href="#" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_06.jpg" class="swiper-lazy" alt="圖說6" />
        </a>
      </div>
      <div class="imgContainer swiper-slide">
        <a href="#" title="">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_07.jpg" class="swiper-lazy" alt="圖說7" />
        </a>
      </div>
    </div>
  </div>
  <!--操控物件可以隨意放，但注意設定要對應到-->
  <!--前一筆-->
  <div class="prevSlider swiperArrow"></div>
  <!--下一筆-->
  <div class="nextSlider swiperArrow"></div>
</div>
  </div>

<!-- tabs:start -->

#### **HTML**

```html
<!-- 廣告輪播   start -->
<div class="adSlider">
  <div class="swiperBox">
    <div class="swiper">
      <div class="swiper-wrapper">
        <!-- 此區塊以下為一筆 -->
        <div class="imgContainer swiper-slide">
          <a href="#" title="">
            <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/ad_01.jpg" class="cover" alt="圖說1" />
          </a>
        </div>
        <!-- 此區塊以上為一筆 -->
        。。。
      </div>
    </div>
  </div>

  <!--操控物件可以隨意放，但注意設定要對應到-->
  <!--前一筆-->
  <div class="prevSlider swiperArrow"></div>
  <!--下一筆-->
  <div class="nextSlider swiperArrow"></div>
</div>
<!-- 廣告輪播   end -->
```

### **css**

```css
.adSlider {
  position: relative;
}
```

#### **JAVASCRIPT**

```javascript
const adSlider = new Swiper('.adSlider .swiper', {
  slidesPerView: 5, //顯示張數
  navigation: {
    nextEl: '.adSlider .nextSlider', //下一張class，無障礙設定關係需要增加.nextSlider
    prevEl: '.adSlider .prevSlider', //前一張class，無障礙設定關係需要增加.prevSlider
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
<!--大圖slider-for-->
<div class="sliderFor">
  <div class="swiperBox">
    <div class="swiper">
      <div class="swiper-wrapper">
        <div class="imgContainer swiper-slide">
          <a href="javascript:;" title="">
            <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg" class="swiper-lazy" alt="圖說1" />
            <span class="caption">圖說1</span>
          </a>
        </div>
        <div class="imgContainer swiper-slide">
          <a href="javascript:;" title="">
            <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/02.jpg" class="swiper-lazy" alt="圖說2" />
            <span class="caption">圖說2</span>
          </a>
        </div>
        <div class="imgContainer swiper-slide">
          <a href="javascript:;" title="">
            <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/03.jpg" class="swiper-lazy" alt="圖說3" />
            <span class="caption">圖說3</span>
          </a>
        </div>
        <div class="imgContainer swiper-slide">
          <a href="javascript:;" title="">
            <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/04.jpg" class="swiper-lazy" alt="圖說4" />
            <span class="caption">圖說4</span>
          </a>
        </div>
        <div class="imgContainer swiper-slide">
          <a href="javascript:;" title="">
            <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/05.jpg" class="swiper-lazy" alt="圖說5" />
            <span class="caption">圖說5</span>
          </a>
        </div>
      </div>
    </div>
    <!--分頁-->
    <div class="pagination"></div>
  </div>
</div>

<!-- slider-for end-->
<!--小圖slider-nav-->

<div class="navSlider">
  <div class="swiperBox">
    <div class="swiper">
      <div class="swiper-wrapper">
        <div class="imgContainer swiper-slide">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg" class="swiper-lazy" alt="圖說1" />
          <span class="caption">圖說1</span>
        </div>
        <div class="imgContainer swiper-slide">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/02.jpg" class="swiper-lazy" alt="圖說2" />
          <span class="caption">圖說2</span>
        </div>
        <div class="imgContainer swiper-slide">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/03.jpg" class="swiper-lazy" alt="圖說3" />
          <span class="caption">圖說3</span>
        </div>
        <div class="imgContainer swiper-slide">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/04.jpg" class="swiper-lazy" alt="圖說4" />
          <span class="caption">圖說4</span>
        </div>
        <div class="imgContainer swiper-slide">
          <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/05.jpg" class="swiper-lazy" alt="圖說5" />
          <span class="caption">圖說5</span>
        </div>
      </div>
    </div>
    <!--操控物件可以隨意放，但注意設定要對應到-->
    <!--前一筆-->
    <div class="prevSlider swiperArrow"></div>
    <!--下一筆-->
    <div class="nextSlider swiperArrow"></div>
  </div>
</div>

<!-- slider-nav end-->
</div>

<!-- tabs:start -->

#### **HTML**

```html

  <!--大圖slider-for-->
  <div class="sliderFor">
    <div class="swiperBox">
      <div class="swiper">
        <div class="swiper-wrapper">
          <!-- 此區塊以下為一筆 -->
          <div class="imgContainer swiper-slide">
            <a href="javascript:;" title="">
              <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg" class="swiper-lazy" alt="圖說1" />
              <span>圖說</span>
            </a>
          </div>
          <!-- 此區塊以上為一筆 -->
          。。。
        </div>
      </div>
      <!--分頁-->
      <div class="pagination"></div>
    </div>
  </div>

  <!-- slider-for end-->
  <!--小圖slider-nav-->

  <div class="navSlider">
    <div class="swiperBox">
      <div class="swiper">
        <div class="swiper-wrapper">
          <!-- 此區塊以下為一筆 -->
          <div class="imgContainer swiper-slide">
            <img data-src="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg" class="swiper-lazy" alt="圖說1" />
            <span>圖說</span>
          </div>
          <!-- 此區塊以上為一筆 -->
          。。。
        </div>
      </div>
      <!--操控物件可以隨意放，但注意設定要對應到-->
      <!--前一筆-->
      <div class="prevSlider swiperArrow"></div>
      <!--下一筆-->
      <div class="nextSlider swiperArrow"></div>
    </div>
    <!-- slider-nav end-->
  </div>
</div>
```

#### **CSS**

```css
.navSlider {
  position: relative;
}
```

#### **JAVASCRIPT**

```javascript
//注意小圖的設定一定要放在大圖的上方
const navSlider = new Swiper('.navSlider .swiper', {
  lazy: true, // lazy load
  preloadImages: false, // 多筆設定lazy時須設定
  centeredSlides: false, // 多筆設定lazy時須設定
  slidesPerView: 4,
  // watchSlidesProgress: true,
  navigation: {
    nextEl: '.navSlider .nextSlider', //下一張class，無障礙設定關係需要增加.nextSlider
    prevEl: '.navSlider .prevSlider', //前一張class，無障礙設定關係需要增加.prevSlider
  },
});

const sliderFor = new Swiper('.sliderFor .swiper', {
  slidesPerView: 1, //顯示張數
  effect: 'fade', //淡入
  fadeEffect: {
    crossFade: true, //上一張淡出，false上一張不淡出，下一張疊在上方
  },
  pagination: {
    el: '.sliderFor .pagination',
    type: 'fraction', //顯示分頁
  },
  lazy: true,
  thumbs: {
    swiper: navSlider, //設定指向到哪個swiper，使用另一個設定的參數
  },
});
```

<!-- tabs:end -->

## Javascript 設定:round_pushpin:

### 關於 slick 按鈕的 title 語系

因應無障礙需求，在左右箭頭需要有替代文字，但往往因為網站有不同語系需求，因此按鈕需要呈現不同語言的替代文字，例如:

<<font color="#009ee7">html</font> lang="<font color="#EE428B">zh-Hant</font>">中按鈕會呈現<<font color="#009ee7">button</font> class="slick-prev" ... title="<font color="#EE428B">前一則</font>">Previous</button>或是
<<font color="#009ee7">html</font> lang="<font color="#EE428B">en</font>" >中按鈕會呈現或是<<font color="#009ee7">button</font> class="<font color="#EE428B">slick-prev</font>" ... title="<font color="#EE428B">previous</font>">Previous</button>，
此時無法用同一種語言因應各種語系，HyUI 提供一組判斷語系之 javascript 設定，語系參照[W3C ISO Language Codes](https://www.w3schools.com/tags/ref_language_codes.asp)，可自行複製到各專案修改語系及對應之替代文字即可。注意：此程式並無預設放入 <font color="#EE428B">hyui.js</font>。

其中，程式是判斷語系字串中的前面字符作為判斷依據，目的是同一語系可能會有分支語系，但以開頭之語系英文字母做判斷。

## main.js 中設定箭頭的語系

```javascript
//無障礙切換swiper箭頭語系
//swiper 箭頭設定
swiperArrows({
  next: '.nextSlider',
  prev: '.prevSlider',
  data: [
    //增加語系請寫在這邊
    {
      lang: 'zh',
      nextText: '下一筆',
      prevText: '上一筆',
    },
  ],
  default: {
    nextText: 'next',
    prevText: 'previous',
  },
});
```

<!--
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
``` -->

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@8/swiper-bundle.min.css" />
<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
.swiperDots{
  position:relative;
  bottom:0px !important;
}
.swiper-slide {
  position:relative;
}
.navSlider,
.bannerSlider,
.adSlider{
  position:relative;
  overflow:hidden;
}
</style>

<script>
const bannerSlider = new Swiper('.bannerSlider .swiper', {
  slidesPerView: 1, //顯示張數
  navigation: {
    nextEl: '.bannerSlider .nextSlider', //下一張class，無障礙設定關係需要增加.nextSlider
    prevEl: '.bannerSlider .prevSlider', //前一張class，無障礙設定關係需要增加.prevSlider
  },
  pagination: {
    //顯示圓點
    el: '.bannerSlider .swiperDots', //圓點 class
    bulletElement: 'button',
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
    nextEl: '.adSlider .nextSlider', //下一張class，無障礙設定關係需要增加.nextSlider
    prevEl: '.adSlider .prevSlider', //前一張class，無障礙設定關係需要增加.prevSlider
  },
  spaceBetween: 20,
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
  autoHeight: false,
  navigation: {
    nextEl: '.navSlider .nextSlider', //下一張class，無障礙設定關係需要增加.nextSlider
    prevEl: '.navSlider .prevSlider', //前一張class，無障礙設定關係需要增加.prevSlider
  },
});

const sliderFor = new Swiper('.sliderFor .swiper', {
  slidesPerView: 1, //顯示張數
  effect: 'fade', //淡入
  fadeEffect: {
    crossFade: true, //上一張淡出，false上一張不淡出，下一張疊在上方
  },
  pagination: {
    el: '.sliderFor .pagination',
    type: 'fraction', //顯示分頁
  },
  lazy: true,
  thumbs: {
    swiper: navSlider, //設定指向到哪個swiper，使用另一個設定的參數
  },
})
</script>
