# Album+Lightbox/相簿(縮圖)列表+燈箱

?>檔案名稱：sass/common/ `_gridflex.scss`<br/>
檔案名稱：sass/ module / `_thumbnail.scss`

HyUI 使用 **fancybox** 的燈箱套件，目前 hyUI vendor 內含 `fancybox` 已經有加入客製化設定，如需要最新版，請到 [fancybox](https://fancyapps.com/docs/ui/fancybox/) 官網參考下載。

## 匯入外掛 fancybox CSS

```html
<!-- 燈箱facybox -->
<link rel="stylesheet" type="text/css" href="vendor/fancybox/fancybox.css" />
```

## 匯入外掛 fancybox js

```html
<!-- 燈箱facybox -->
<script src="vendor/fancybox/fancybox.js"></script>
```

此為相簿列表模組示範範例。當相簿需要觸發的連結區塊，以及燈箱區塊設定放大瀏覽照片時，
請將 **圖片連結**寫入 `href` 裡，並在 `a `裡加上 `data-fancybox` 、 `data-caption` 及 `data-alt`<br/>

## Thumbnail / 卡片式縮圖

- flexEqual_2 為 `2` 個一列<br/>
- flexEqual_3 為 `3` 個一列<br/>
- flexEqual_4 為 `4` 個一列<br/>
- flexEqual_5 為 `5` 個一列<br/>

<div class="flexEqual_3">
  <div class="flexSet">
    <div class="thumbnail">
      <a href="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg" data-fancybox="images" data-caption="第1張圖說" data-alt="第1張圖說">
        <div class="imgContainer">
            <img src="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg" alt="圖說1" />
        </div>
        <div class="caption">
          <time>2018-01-01</time>
          <h3>標題</h3>
          <p>內文</p>
        </div>
      </a>
    </div>
    <div class="thumbnail">
      <a href="https://hywebu00.github.io/hyui_flex/images/demo/02.jpg" data-fancybox="images" data-caption="第2張圖說" data-alt="第2張圖說">
        <div class="imgContainer">
            <img src="https://hywebu00.github.io/hyui_flex/images/demo/02.jpg" alt="圖說2" />
        </div>
        <div class="caption">
          <time>2018-01-01</time>
          <h3>標題</h3>
          <p>內文</p>
        </div>
      </a>
    </div>
    <div class="thumbnail">
      <a href="https://hywebu00.github.io/hyui_flex/images/demo/03.jpg" data-fancybox="images" data-caption="第3張圖說" data-alt="第3張圖說">
        <div class="imgContainer">
            <img src="https://hywebu00.github.io/hyui_flex/images/demo/03.jpg" alt="圖說3" />
        </div>
        <div class="caption">
          <time>2018-01-01</time>
          <h3>標題</h3>
          <p>內文</p>
        </div>
      </a>
    </div>
  </div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<!-- grid:flex -->
<section class="flexEqual_3">
  <div class="container">
    <div class="flexSet">
      <!-- 此區塊以下為一筆 -->
      <div class="thumbnail">
        <a href="https://source.unsplash.com/random/1" data-fancybox="images" data-caption="第1張圖說" data-alt="第1張圖說">
          <div class="imgContainer">
            <picture>
              <source media="(min-width: 1200px)" data-srcset="https://source.unsplash.com/random/1" />
              <source media="(min-width: 992px)" data-srcset="https://source.unsplash.com/random/1" />
              <source media="(min-width: 576px)" data-srcset="https://source.unsplash.com/random/1" />
              <source media="(max-width: 575px)" data-srcset="https://source.unsplash.com/random/1" />
              <img data-src="https://source.unsplash.com/random/1" class="lazy" alt="圖說1" />
              <noscript><img src="https://source.unsplash.com/random/1" alt="圖說1" /></noscript>
            </picture>
          </div>
          <div class="caption">
            <time>2018-01-01</time>
            <h3>標題</h3>
            <p>內文</p>
          </div>
        </a>
      </div>
      <!-- 此區塊以上為一筆 -->
      。 。 。
    </div>
  </div>
</section>
```

<!-- tabs:end -->

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/vendor/fancybox/fancybox.css"/>
