# Category / 分類目錄

?>檔案名稱：sass/element/`category.scss`

<div class="demo">
<div class="category">
    <ul>
        <li><a class="active" href="#">標籤1 <span>10</span></a></li>
        <li><a href="#">標籤2 <span>5</span></a></li>
        <li><a href="#">標籤3 <span>4</span></a></li>
        <li><a href="#">標籤4 <span>6</span></a></li>
        <li><a href="#">標籤5 <span>12</span></a></li>
        <li><a href="#">標籤6 <span>9</span></a></li>
        <li><a href="#">標籤7 <span>5</span></a></li>
        <li><a href="#">標籤8 <span>2</span></a></li>
    </ul>
</div></div>

> 範例：可加入數量統計狀態

可於連結內，放置`span`標籤，讓程式帶入筆數數值即可。

<!-- tabs:start -->

#### **HTML**

```html
<div class="category">
  <ul>
    <li>
      <a href="#">標籤1 <span>10</span></a>
    </li>
    <li>
      <a href="#">標籤2 <span>5</span></a>
    </li>
    <li>
      <a href="#">標籤3 <span>4</span></a>
    </li>
    <li>
      <a href="#">標籤4 <span>6</span></a>
    </li>
    <li>
      <a href="#">標籤5 <span>12</span></a>
    </li>
    <li>
      <a href="#">標籤6 <span>9</span></a>
    </li>
    <li>
      <a href="#">標籤7 <span>5</span></a>
    </li>
    <li>
      <a href="#">標籤8 <span>2</span></a>
    </li>
  </ul>
</div>
```

#### **JavaScript**

```javascript
function categoryActive() {
  const categoryList = document.querySelectorAll('.category');
  categoryList.forEach((i) => {
    const item = i.querySelectorAll('a');
    item.forEach((tag) => {
      tag.addEventListener('click', (e) => {
        e.preventDefault();
        removeClass(item);
        e.target.classList.add('active');
      });
    });
  });

  function removeClass(item) {
    item.forEach((i) => {
      i.classList.remove('active');
    });
  }
}
categoryActive();
```

<!-- tabs:end -->

<!-- <iframe height="265" style="width: 100%;" scrolling="no" title="Category / 分類目錄" src="https://codepen.io/u00hyui/embed/poNmBqz?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/poNmBqz'>Category / 分類目錄</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe> -->

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<style>
.category {
  text-align: left;
  margin: 4em auto;
}
.category ul {
  display: flex;
  flex-wrap: wrap;
}
.category ul li {
  margin: 0px 3px 3px 0px;
  display: block;
}
.demo .category a {
  border: 1px solid #aaa;
  padding: 0.25em 0.75em;
  display: block;
  color: #333;
  font-size: 0.875rem;
  box-sizing: border-box;
  border: 1px solid #aaa;
   border-radius: 4px;
}
.category a:before {
  content: "#";
  margin-right: 0.25em;
}
.category a:hover, .category a:focus, .category a.active {
  color: #fff;
  box-shadow: none;
  background: linear-gradient(to bottom, #06c, #004080);
}
.category a span {
  font-size: 0.813em;
}
.category a span:before {
  content: "(";
  display: inline-block;
}
.category a span:after {
  content: ")";
  display: inline-block;
}
</style>
<script>
  function categoryActive() {
  const categoryList = document.querySelectorAll('.category');
  categoryList.forEach((i) => {
    const item = i.querySelectorAll('a');
    item.forEach((tag) => {
      tag.addEventListener('click', (e) => {
        e.preventDefault();
        removeClass(item);
        e.target.classList.add('active');
      });
    });
  });
  function removeClass(item) {
    item.forEach((i) => {
      i.classList.remove('active');
    });
  }
}
categoryActive();
</script>
