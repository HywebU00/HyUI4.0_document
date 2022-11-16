# Flex grid system

?>格線系統：以 **flex** 為計算基礎，主要功能是分割欄位。
檔案名稱：sass / common / `grid-flex.scss`

HyUI 的 flex grid system 分割方式 分為 **均分** 和 **自由分配**

### 均分

?>每欄 **欄寬都相同** ，預設 2-12 欄。

> 算式：100% ÷ 欄數

<section class="flexEqual_2">
          <div class="container">
            <h4>均分 2 欄</h4>
            <div class="flexSet">
              <div class="col">
                <h3>title 1</h3>
                <p>col Lorem ipsum dolor sit amet, quos similique?</p>
              </div>
              <div class="col">
                <h3>title 2</h3>
                <p>col Lorem ipsum dolor sit</p>
              </div>
            </div>
          </div>
        </section>
        <!-- 3、 -->
        <section class="flexEqual_3">
          <div class="container">
            <h4>均分 3 欄</h4>
            <div class="flexSet">
              <div class="col">
                <h3>title 1</h3>
                <p>col Lorem ipsum dolor sit amet, quos similique?</p>
              </div>
              <div class="col">
                <h3>title 2</h3>
                <p>col Lorem ipsum dolor sit amet, quos similique?</p>
              </div>
              <div class="col">
                <h3>title 3</h3>
                <p>col Lorem ipsum dolor sit amet, quos similique?</p>
              </div>
            </div>
          </div>
        </section>
        <!-- 4、 -->
        <section class="flexEqual_4">
          <div class="container">
            <h4>均分 4 欄</h4>
            <div class="flexSet">
              <div class="col">
                <h3>title 1</h3>
                <p>col Lorem ipsum dolor sit amet, quos similique?</p>
              </div>
              <div class="col">
                <h3>title 2</h3>
                <p>col Lorem ipsum dolor sit amet, quos similique?</p>
              </div>
              <div class="col">
                <h3>title 3</h3>
                <p>col Lorem ipsum dolor sit amet, quos similique?</p>
              </div>
              <div class="col">
                <h3>title 4</h3>
                <p>col Lorem ipsum dolor sit amet, quos similique?</p>
              </div>
            </div>
          </div>
        </section>
<!-- tabs:start -->

#### **CSS**

```sass
// step 0、設定共用的 margin gutter
$mGutter: 4px;

.flexSet{
    // 啟動flex
    // 位置：sass/sass/common/mixins/_extend.scss
    @extend %flexSet;


    // step 2、子層設定欄寬，可設定斷點
    .col{
        @include flexXsEqual(1, 0px);
        @include flexSmEqual(2, $mGutter);
        @include flexMdEqual(4, $mGutter);
        @include flexLgEqual(8, $mGutter);
        @include gutter();
    }
}
```

  <!-- tabs:end -->

<!-- <iframe height="500" style="width: 100%;" scrolling="no" title="flex grid system equal" src="https://codepen.io/u00hyui/embed/dyWyGar?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/dyWyGar">
  flex grid system equal</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe> -->

### 自由分配

?> **每欄欄寬不相同**，加總等於`12`
可應用在**3+9**、**4+8**、**5+7**、**3+6+3** ...等非均分的分割。

> 算式：(100% ÷ 12) × 欄數

<section class="flex_3_6_3">
          <div class="container">
            <h3>flex_3_6_3</h3>
            <div class="flexSet">
              <div class="col">
                <h3>次標題一</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quo facilis sequi quidem velit quae voluptas temporibus aliquam quasi doloremque sunt? Sapiente ea dolorem dolore sit itaque facere sunt voluptatem deleniti!</p>
              </div>
              <div class="col">
                <h3>次標題二</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quo facilis sequi quidem velit quae voluptas temporibus aliquam quasi doloremque sunt? Sapiente ea dolorem dolore sit itaque facere sunt voluptatem deleniti!</p>
              </div>
              <div class="col">
                <h3>次標題三</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quo facilis sequi quidem velit quae voluptas temporibus aliquam quasi doloremque sunt? Sapiente ea dolorem dolore sit itaque facere sunt voluptatem deleniti!</p>
              </div>
            </div>
          </div>
        </section>

<!-- tabs:start -->

#### **CSS**

```sass
// step 0、設定共用的 margin gutter
$mGutter: 4px;

.flex_8_4{
    // step 1、父層啟動flex
    @extend %flexSet;

    // step 2、子層設定欄寬，可設定斷點
    .col{
        @include flexXs(12, 0px);
        @include flexSm(6, $mGutter);
        @include flexMd(8, $mGutter);
        @include flexLg(8, $mGutter);
        @include gutter();

        &:nth-child(2){
            @include flexXs(12, 0px);
            @include flexSm(6, $mGutter);
            @include flexMd(4, $mGutter);
            @include flexLg(4, $mGutter);
        }
    }
}
```

<!-- tabs:end -->

### 混合運用

?> **均分** Ｘ **自由分配**

<section class="mixEqual_2">
  <div class="container">
    <h4>均分 併 自由分配</h4>
    <div class="flexSet">
      <div class="col">
        <h3>次標題一</h3>
        <section class="inner_4_8">
          <div class="imgContainer">
            <picture>
              <source media="(min-width: 1200px)" data-srcset="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg">
              <source media="(min-width: 992px)" data-srcset="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg">
              <source media="(min-width: 576px)" data-srcset="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg">
              <source media="(max-width: 575px)" data-srcset="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg">
              <img src="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg">
              <noscript><img src="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg"></noscript>
            </picture>
          </div>
          <div class="text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum nam, aperiam error accusamus, distinctio laboriosam minus nesciunt cum labore voluptate consectetur magni, illum in recusandae. Optio, ab voluptatibus suscipit magnam.</div>
        </section>
      </div>
      <div class="col">
        <h3>次標題二</h3>
        <section class="inner_4_8">
          <div class="imgContainer">
            <picture>
              <source media="(min-width: 1200px)" data-srcset="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg">
              <source media="(min-width: 992px)" data-srcset="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg">
              <source media="(min-width: 576px)" data-srcset="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg">
              <source media="(max-width: 575px)" data-srcset="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg">
              <img src="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg">
              <noscript><img src="https://hywebu00.github.io/hyui_flex/images/demo/01.jpg"></noscript>
            </picture>
          </div>
          <div class="text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum nam, aperiam error accusamus, distinctio laboriosam minus nesciunt cum labore voluptate consectetur magni, illum in recusandae. Optio, ab voluptatibus suscipit magnam.</div>
        </section>
      </div>
    </div>
  </div>
</section>

<!-- tabs:start -->

#### **CSS**

```sass
// step 0、設定共用的 margin gutter
$m-gutter: 4px;

// 綜合
.mixEqual_2{
    .flexSet{
        // step 1、父層啟動flex
        @extend %flexSet;
        // step 2、子層設定欄寬，可設定斷點
        .col{
            @include flexXsEqual(1, 0px);
            @include flexSmEqual(2, $mGutter);
            @include flexMdEqual(2, $mGutter);
            @include flexLgEqual(2, $mGutter);
            padding: 1em;
        }
    }

    .inner_4_8{
        // step 1、父層啟動flex
        @extend %flexSet;
        // step 2、子層設定欄寬，可設定斷點
        div{
            @include flexXs(12, 0px);
            @include flexSm(4, $mGutter);
            @include flexMd(4, $mGutter);
            @include flexLg(4, $mGutter);

            &:last-child{
                @include flexXs(12, 0px);
                @include flexSm(8, $mGutter);
                @include flexMd(8, $mGutter);
                @include flexLg(8, $mGutter);
            }
        }
    }
}
```

<!-- tabs:end -->

<!-- <iframe height="500" style="width: 100%;" scrolling="no" title="flex grid system mix" src="https://codepen.io/u00hyui/embed/eYWYZZK?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/eYWYZZK">
  flex grid system mix</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe> -->

?>**附加說明**<br> 1. 二個數值代表順序為：**欄數**、**margin gutter**
值後面，務必加上**單位**（%、px、em），**數值為『0』一樣要加單位**。</br> 2. **margin gutter** 的數值是**雙側的總和**，例如：**$mGutter: 20px**，欄寬左右各扣除 `10px`，以`space-between`達成對齊的效果</br> 3. flex grid 算式複雜，須配合斷點更改欄數，故 flex grid 的斷點採用`min-width`，極小尺寸為 screen-xs-flex:320px

<!-- <div class="box">
    <h3>附加說明</h3>
    <ol>
        <li>二個數值代表順序為：<span class="focus2">欄數</span>、<span class="focus2">margin gutter</span></li>
        <li>數值後面，<span class="focus">務必加上單位（%、px、em）</span>，數值為『0』一樣要加單位。</li>
    <li>margin gutter的數值是<span class="focus2">雙側的總和</span>，</br>例如：$m-gutter: 20px，欄寬左右各扣除10px，以<span class="focus2">space-between</span>達成對齊的效果</li>
    <li>flex grid算式複雜，須配合斷點更改欄數，故 flex grid 的斷點採用<span class="focus2">min-width</span>，極小尺寸為<span class="focus2"><span class="focus">screen-xs-flex: 320px</span></span></li>
</ol>
</div> -->
<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<style>
    .col{
        background-color:#225d6214;
    }
    .col p , .col h3{
        color:#777;
    }
    h4{
    margin-bottom: 0.5em;
    }
    .mixEqual_2 h3{
        margin-top:0em;
    }
    .text{
         color:#777;
    }
</style>
