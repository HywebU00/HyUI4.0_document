# Marquee / 跑馬燈

###### tags: `HyUI`

檔案名稱：sass/modual/\_marquee.scss

HyUI 提供跑馬燈的範例，有使用 <font color="#009ee7">slick</font> 的輪播模組，需先在網頁中匯入外掛 CSS 及 js，可參考模組 [Slider 圖片輪播](/VkhALd3wTYSt_ctD6W0XPQ)說明。

<div class="marquee">
  <h3>跑馬燈</h3>
  <div class="swiperBox">
    <div class="swiper">
      <div class="swiper-wrapper">
        <div class="swiper-slide">
          <a href="javascript:;"><span>2018-11-13</span>因尼莎颱風來襲，7/31下午2時之我國化學物質管理政策綱領第一次跨部會研商會取消。</a>
        </div>
        <div class="swiper-slide">
          <a href="javascript:;"><span>2018-11-13</span>因尼莎颱風來襲，7/31下午2時之我國化學物質管理政策綱領第一次跨部會研商會取消。</a>
        </div>
        <div class="swiper-slide">
          <a href="javascript:;"><span>2018-11-13</span>因尼莎颱風來襲，7/31下午2時之我國化學物質管理政策綱領第一次跨部會研商會取消。</a>
        </div>
        <div class="swiper-slide">
          <a href="javascript:;"><span>2018-11-13</span>因尼莎颱風來襲，7/31下午2時之我國化學物質管理政策綱領第一次跨部會研商會取消。</a>
        </div>
      </div>
    </div>
    <!-- swiper 往上-->
    <div class="marquee-arrow marquee-prev"></div>
    <!-- swiper 往下-->
    <div class="marquee-arrow marquee-next"></div>
  </div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="marquee">
  <h3>跑馬燈</h3>
  <div class="swiperBox">
    <div class="swiper">
      <div class="swiper-wrapper">
        <div class="swiper-slide">
          <a href="javascript:;"><span>2018-11-13</span>因尼莎颱風來襲，7/31下午2時之我國化學物質管理政策綱領第一次跨部會研商會取消。</a>
        </div>
        <div class="swiper-slide">
          <a href="javascript:;"><span>2018-11-13</span>因尼莎颱風來襲，7/31下午2時之我國化學物質管理政策綱領第一次跨部會研商會取消。</a>
        </div>
        <div class="swiper-slide">
          <a href="javascript:;"><span>2018-11-13</span>因尼莎颱風來襲，7/31下午2時之我國化學物質管理政策綱領第一次跨部會研商會取消。</a>
        </div>
        <div class="swiper-slide">
          <a href="javascript:;"><span>2018-11-13</span>因尼莎颱風來襲，7/31下午2時之我國化學物質管理政策綱領第一次跨部會研商會取消。</a>
        </div>
      </div>
    </div>
    <!-- swiper 往上-->
    <div class="marquee-arrow marquee-prev"></div>
    <!-- swiper 往下-->
    <div class="marquee-arrow marquee-next"></div>
  </div>
</div>
```

#### **JAVASCRIPT**

```javascript
const marqueeSwiper = new Swiper('.marquee .swiper', {
  direction: 'vertical',
  // 切換點
  // 切換箭頭
  navigation: {
    nextEl: '.marquee .marquee-next', //自行設定樣式
    prevEl: '.marquee .marquee-prev', //自行設定樣式
    disabledClass: '.marquee marquee-arrow-disabled', //不可點選樣式
  },
});
```

<!-- tabs:end -->

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@8/swiper-bundle.min.css" />
<style>
.ui-infobar{
max-width:95%;
}
.markdown-body{
max-width:95%;
}
</style>

<script>
  const marqueeSwiper = new Swiper('.marquee .swiper', {
  direction: 'vertical',
  // 切換點
  // 切換箭頭
  navigation: {
    nextEl: '.marquee .marquee-next', //自行設定樣式
    prevEl: '.marquee .marquee-prev', //自行設定樣式
    disabledClass: '.marquee marquee-arrow-disabled', //不可點選樣式
  },
});
</script>
