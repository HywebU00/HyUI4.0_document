# Tag / 標籤

?>檔案名稱：sass/ element /`tag.scss`

此區塊可用於 `列表頁` 、 `內容頁`，屬於文章或資料類型的多重關鍵字標籤

<div class="demo">
<div class="tag">
    <ul>
        <li><a href=javascript:;>文章標籤1</a></li>
        <li><a href=javascript:;>文章標籤2</a></li>
        <li><a href=javascript:;>文章標籤3</a></li>
        <li><a href=javascript:;>文章標籤4</a></li>
        <li><a href=javascript:;>文章標籤5</a></li>
    </ul>
</div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="tag">
  <ul>
    <li><a href="#">文章標籤1</a></li>
    <li><a href="#">文章標籤2</a></li>
    <li><a href="#">文章標籤3</a></li>
    <li><a href="#">文章標籤4</a></li>
    <li><a href="#">文章標籤5</a></li>
  </ul>
</div>
```

<!-- tabs:end -->

<!-- <iframe height="265" style="width: 100%;" scrolling="no" title="Tag / 標籤" src="https://codepen.io/u00hyui/embed/KKWVEpL?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/KKWVEpL'>Tag / 標籤</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe> -->

## 內容頁範例

<section class="demo">
    <h3 class="title">
  iPhone 13 傳將於 9/14 亮相，9/24 正式上市</h3>
<div class="tag">
  <ul>
    <li><a href=javascript:;>iphone SE</a></li>
    <li><a href=javascript:;>iphone XS</a></li>
    <li><a href=javascript:;>蘋果</a></li>
  </ul>
</div>
</section>
<section class="cp">
  <!-- tag 文章標籤 -->
  <p><a href="#">連結文字樣式 </a>隨著蘋果開發者大會（WWDC）落幕，果粉目光轉擺在接下來蘋果（Apple）的大活動──iPhone 發表會。雖然去年 iPhone 12 系列延到 10 月才推出，不過許多人都認為，今年新 iPhone 仍會維持傳統，9 月時亮相。據 Wedbush 分析師 Dan Ives 近期給客戶的報告顯示，iPhone 13 可能於 9 月第三週亮相，按照蘋果過去於週二舉辦發表會的規則推算，iPhone 13 應於美國時間 9 月 14 日亮相，且會在隔一週的週五（9 月 24 日）正式上市。</p>
</section>

<!-- tabs:start -->

#### **HTML**

```html
<h2 class="title">iPhone 13 傳將於 9/14 亮相，9/24 正式上市</h2>
<div class="tag">
  <ul>
    <li><a href="#">iphone SE</a></li>
    <li><a href="#">iphone XS</a></li>
    <li><a href="#">蘋果</a></li>
  </ul>
</div>
<section class="cp">
  <!-- tag 文章標籤 -->
  <p>
    <a href="#">連結文字樣式 </a>隨著蘋果開發者大會（WWDC）落幕，果粉目光轉擺在接下來蘋果（Apple）的大活動──iPhone 發表會。雖然去年 iPhone 12 系列延到 10 月才推出，不過許多人都認為，今年新 iPhone 仍會維持傳統，9 月時亮相。據 Wedbush 分析師 Dan Ives 近期給客戶的報告顯示，iPhone 13 可能於 9
    月第三週亮相，按照蘋果過去於週二舉辦發表會的規則推算，iPhone 13 應於美國時間 9 月 14 日亮相，且會在隔一週的週五（9 月 24 日）正式上市。
  </p>
</section>
```

<!-- tabs:end -->

<!-- <iframe height="400" style="width: 100%;" scrolling="no" title="tag內容頁範例" src="https://codepen.io/u00hyui/embed/jOBjJab?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/jOBjJab">
  tag內容頁範例</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe> -->

## 列表頁範例

<h3 class="title">最新消息</h3>
<section class="lp demo">
  <div class="list">
    <ul>
      <li>
        <a href="#">
          <span class="num">1</span> 颱風逼近軍民齊心加強防颱戒備 <span class="dept">(服務照顧處)</span>
          <time>2018-03-09</time>
        </a>
        <div class="tag">
          <ul>
            <li><a href=javascript:;>文章標籤1</a></li>
            <li><a href=javascript:;>文章標籤2</a></li>
            <li><a href=javascript:;>文章標籤3</a></li>
            <li><a href=javascript:;>文章標籤4</a></li>
            <li><a href=javascript:;>文章標籤5</a></li>
          </ul>
        </div>
      </li>
      <li>
        <a href="#">
          <span class="num">2</span> 東坑微電網示範將到期縣府盼由台電承接 <span class="dept"> (就養養護處)</span>
          <time>2018-03-09</time>
        </a>
        <div class="tag">
          <ul>
            <li><a href=javascript:;>文章標籤1</a></li>
            <li><a href=javascript:;>文章標籤2</a></li>
            <li><a href=javascript:;>文章標籤3</a></li>
            <li><a href=javascript:;>文章標籤4</a></li>
            <li><a href=javascript:;>文章標籤5</a></li>
          </ul>
        </div>
      </li>
      <li>
        <a href="#">
          <span class="num">3</span> 公務員高普考10日登場縣府謹慎試務 <span class="dept"> (就學就業處)</span>
          <time>2018-03-09</time>
        </a>
        <div class="tag">
          <ul>
            <li><a href=javascript:;>文章標籤1</a></li>
            <li><a href=javascript:;>文章標籤2</a></li>
            <li><a href=javascript:;>文章標籤3</a></li>
            <li><a href=javascript:;>文章標籤4</a></li>
            <li><a href=javascript:;>文章標籤5</a></li>
          </ul>
        </div>
      </li>
    </ul>
  </div>
</section>

<!-- tabs:start -->

#### **HTML**

```html
<h2 class="title">最新消息</h2>
<section class="lp">
  <div class="list">
    <ul>
      <li>
        <a href="#">
          <span class="num">1</span> 颱風逼近軍民齊心加強防颱戒備 <span class="dept">(服務照顧處)</span>
          <time>2018-03-09</time>
        </a>
        <div class="tag">
          <ul>
            <li><a href="#">文章標籤1</a></li>
            <li><a href="#">文章標籤2</a></li>
            <li><a href="#">文章標籤3</a></li>
            <li><a href="#">文章標籤4</a></li>
            <li><a href="#">文章標籤5</a></li>
          </ul>
        </div>
      </li>
      <li>
        <a href="#">
          <span class="num">2</span> 東坑微電網示範將到期縣府盼由台電承接 <span class="dept"> (就養養護處)</span>
          <time>2018-03-09</time>
        </a>
        <div class="tag"></div>
      </li>
    </ul>
  </div>
</section>
```

<!-- tabs:end -->
<!-- <iframe height="550" style="width: 100%;" scrolling="no" title="tag列表頁範例" src="https://codepen.io/u00hyui/embed/vYxqMBw?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/vYxqMBw">
  tag列表頁範例</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe> -->

<style>
.demo .tag {
  margin-bottom: 1em;
  position: relative;

}
.demo .tag:before {
    content: '';
    width: 16px;
    height: 16px;
    position: absolute;
    left: 0;
    top: 0.5em;
    background: url(https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_tag.svg) no-repeat center center;
    background-size: 16px;
  }
.demo .tag ul{
      margin: 0;
  padding: 0;
  list-style: none;
    display: flex;
    flex-wrap: wrap;
    margin-left: 1.5em;
}
.demo .tag li {
      margin: 0 0.5em 0.5em 0;
      flex: 0 0 auto;
    }

.demo .tag a {
        display: block;
        font-size: 0.938em;
        border: 1px solid #ddd;
        padding: 0.2em 0.75em;
        color:#222;
        font-weight:400;
        text-decoration:none;
      }
.lp .list>ul {
    list-style-type: none;
    padding: 0;
    border-top: 2px solid #06c;
}
.lp .list>ul>li{
    padding: 1em 0;
    border-bottom: 1px solid #DDD;
    position: relative;
}
.lp .list>ul>li>a {
    display: block;
    padding-left: 2em;
    position: relative;
    line-height: 1.45em;
    color: #222;
    text-decoration: none;
}
.lp .list>ul>li>a .num {
    width: 1.5em;
    text-align: right;
    position: absolute;
    top: 0;
    left: 0;
}
.lp .list>ul>li time {
    display: block;
    color: #AAA;
    font-size: .938em;
}
.lp .list>ul>li .tag{
      margin-bottom: 0em;
}
</style>
