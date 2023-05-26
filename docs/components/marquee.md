# Marquee / 跑馬燈

?>檔案名稱：sass/ module /\_marquee.scss

HyUI 提供跑馬燈的範例，有使用 `slick` 的輪播模組，需先在網頁中匯入外掛 CSS 及 js，可參考模組 [Slider 圖片輪播](/VkhALd3wTYSt_ctD6W0XPQ)說明。

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
                  <button class="marquee-arrow prevSlider"></button>
                  <!-- swiper 往下-->
                  <button class="marquee-arrow nextSlider"></button>
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

#### **JavaScript**

```javascript
const marqueeSwiper = new Swiper('.marquee .swiper', {
  direction: 'vertical',
  // 切換點
  // 切換箭頭
  navigation: {
    nextEl: '.marquee .nextSlider', //自行設定樣式
    prevEl: '.marquee .prevSlider', //自行設定樣式
    disabledClass: '.marquee marquee-arrow-disabled', //不可點選樣式
  },
});
```

<!-- tabs:end -->

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4/css/style.css" />
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@8/swiper-bundle.min.css" />
<style>
  .demo{
    margin:4em 0;
  }
</style>

<script>
  const marqueeSwiper = new Swiper('.marquee .swiper', {
  direction: 'vertical',
  // 切換點
  // 切換箭頭
  navigation: {
      nextEl: '.marquee .nextSlider', //自行設定樣式
      prevEl: '.marquee .prevSlider', //自行設定樣式
      disabledClass: '.marquee marquee-arrow-disabled', //不可點選樣式
    },
});
</script>
