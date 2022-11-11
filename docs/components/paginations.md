# Paginations / 分頁導覽

?>檔案名稱：sass/modual/`paginations.scss`

## 基本樣式

  <div class="demo">
  <div class="pagination">
              <form action="">
                <div class="formInline">
                  <div class="total">
                    共<span>308</span>筆資料，第<span>1/18</span>頁，每頁顯示
                    <select name="" id="" aria-label="每頁顯示">
                      <option value="">10</option>
                      <option value="">20</option>
                      <option value="">30</option>
                      <option value="">40</option>
                    </select>
                    筆， <input type="button" value="確定" class="btn btnSubmit" />
                  </div>
                </div>
              </form>
              <ul class="page">
                <li class="first"><a href=javascript:; title="第一頁">第一頁 </a></li>
                <li class="prev"><a href=javascript:; title="回上一頁">回上一頁 </a></li>
                <li class="active"><a href=javascript:;>1</a></li>
                <li><a href=javascript:;>2</a></li>
                <li><a href=javascript:;>3</a></li>
                <li><a href=javascript:;>4</a></li>
                <li><a href=javascript:;>5</a></li>
                <li><a href=javascript:;>6</a></li>
                <li><a href=javascript:;>7</a></li>
                <li><a href=javascript:;>8</a></li>
                <li><a href=javascript:;>9</a></li>
                <li><a href=javascript:;>10</a></li>
                <li class="next"><a href=javascript:; title="下一頁">下一頁 </a></li>
              </ul>
            </div>
  </div>

<!-- tabs:start -->

#### **HTML**

```html
<!-- Pagination -->
<div class="pagination">
  <form action="">
    <div class="formInline">
      <div class="total">
        共<span>308</span>筆資料，第<span>1/18</span>頁，每頁顯示
        <select name="" id="" aria-label="每頁顯示">
          <option value="">10</option>
          <option value="">20</option>
          <option value="">30</option>
          <option value="">40</option>
        </select>
        筆， <input type="button" value="確定" class="btn btnSubmit" />
      </div>
    </div>
  </form>
  <ul class="page">
    <li class="first"><a href="#" title="第一頁">第一頁 </a></li>
    <li class="prev"><a href="#" title="回上一頁">回上一頁 </a></li>
    <li class="active"><a href="#">1</a></li>
    <li><a href="#">2</a></li>
    <li><a href="#">3</a></li>
    <li><a href="#">4</a></li>
    <li><a href="#">5</a></li>
    <li><a href="#">6</a></li>
    <li><a href="#">7</a></li>
    <li><a href="#">8</a></li>
    <li><a href="#">9</a></li>
    <li><a href="#">10</a></li>
    <li class="next"><a href="#" title="下一頁">下一頁 </a></li>
  </ul>
</div>
```

<!-- tabs:end -->

<!-- <iframe height="265" style="width: 100%;" scrolling="no" title="Paginations / 分頁導覽1" src="https://codepen.io/u00hyui/embed/JjWobWJ?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/JjWobWJ'>Paginations / 分頁導覽1</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe> -->

## 不含 Input 的分頁導覽

<div class="demo">
    <div class="pagination">
    <div class="total"> 共<span>308</span>筆資料，第<span>1/18</span>頁，</div>
    <div class="items">每頁顯示 <a href=javascript:;>20</a> <a href=javascript:;>40</a> <a href=javascript:;>60</a> 筆 </div>
    <ul class="page">
        <li class="first"><a href=javascript:; title="第一頁">第一頁</a></li>
        <li class="prev"><a href=javascript:; title="回上一頁">回上一頁 </a></li>
        <li class="active"><a href=javascript:;>1</a></li>
        <li class="xs_hidden"><a href=javascript:;>2</a></li>
        <li class="xs_hidden"><a href=javascript:;>3</a></li>
        <li class="xs_hidden"><a href=javascript:;>4</a></li>
        <li class="xs_hidden"><a href=javascript:;>5</a></li>
        <li class="next"><a href=javascript:; title="下一頁">下一頁</a></li>
        <li class="last"><a href=javascript:; title="最後一頁">最後一頁</a></li>
    </ul>
</div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="pagination">
  <div class="total">共<span>308</span>筆資料，第<span>1/18</span>頁，</div>
  <div class="items">每頁顯示 <a href="#">20</a> <a href="#">40</a> <a href="#">60</a> 筆</div>
  <ul class="page">
    <li class="first"><a href="#" title="第一頁">第一頁</a></li>
    <li class="prev"><a href="#" title="回上一頁">回上一頁 </a></li>
    <li class="active"><a href="#">1</a></li>
    <!-- 可以選擇在叫小尺寸時選擇隱藏部分按鈕 -->
    <li class="xs_hidden"><a href="#">2</a></li>
    <li class="xs_hidden"><a href="#">3</a></li>
    <li class="xs_hidden"><a href="#">4</a></li>
    <li class="xs_hidden"><a href="#">5</a></li>
    <li class="next"><a href="#" title="下一頁">下一頁</a></li>
    <li class="last"><a href="#" title="最後一頁">最後一頁</a></li>
  </ul>
</div>
```

<!-- tabs:end -->

<!-- <iframe height="265" style="width: 100%;" scrolling="no" title="Paginations / 分頁導覽2" src="https://codepen.io/u00hyui/embed/zYZxowN?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/zYZxowN'>Paginations / 分頁導覽2</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe> -->

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />

<style>
.demo{
    margin:4em 0;
}
.demo .pagination .page li.active a ,.demo .pagination .page li:hover a{
    color: #fff !important;
    background: #06c;
    border: #0059b3 solid 1px;}
@media screen and (max-width: 575px){
    .xs_hidden{
       display:none;
    }
}
 
</style>
