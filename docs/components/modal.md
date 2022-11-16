# Modal 彈出對話框

?>檔案名稱：sass/ module / `modal.scss`

此 **燈箱模組** 為示範範例。此功能倚賴 [fancybox](https://fancyapps.com/fancybox/) 的燈箱套件。<br>
頁面需要觸發的連結按鈕，以及燈箱區塊設定，使用以下的程式碼範例，
可自行修改所需樣式，可於 `scss` 修改 **顏色**、 **大小** 、 **動畫效果** ...等。

<button class="btn demo" data-fancybox data-src="#dialog-content">
  開啟視窗
</button>
<div class='modal' id="dialog-content" style="display:none;">
    <!--     div內的內容可以自行設定 -->
  <h2>標題</h2>
  <p>內文</p>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<button class="btn" data-fancybox data-src="#dialog-content">開啟視窗</button>
<div class="modal" id="dialog-content" style="display:none;">
  <!-- div內的內容可以自行設定 -->
  <h2>標題</h2>
  <p>內文</p>
</div>
```

#### **JavaScript**

```javascript
Fancybox.bind('[data-fancybox]', {
  // Your options go here
});
```

<!-- tabs:end -->

<!-- <iframe height="450" style="width: 100%;" scrolling="no" title="Modal 彈出對話框" src="https://codepen.io/u00hyui/embed/JjWGaWa?height=265&theme-id=dark&default-tab=js,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/JjWGaWa">Modal 彈出對話框</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>) on <a href="https://codepen.io">CodePen</a>.
</iframe> -->

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<style>
  .modal{
    width: 400px;
    height: 300px;
    background: #FFF;
    padding: 1.5em;
    display:none;
    border-radius: 8px;
    box-shadow: 1px 1px 15px RGBA(0, 0, 0, 0.5);
  }
  .modal h2{
    border-bottom:1px solid #06c;
    padding-bottom:0.5em;
    margin-bottom: 0em;
  }
  .fancybox__content>.carousel__button.is-close{
    top: 0;
    color: #888;
  }
  .carousel__button svg{
        filter: none;
  }
  .demo{
    margin:4em 0;
  }
</style>
