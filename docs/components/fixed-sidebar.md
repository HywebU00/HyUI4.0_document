# Fixed_sidebar / 固定側邊欄

?>檔案名稱：sass/ module / `fixed_sidebar.scss`

HyUI 提供一個固定`側邊欄`的作法，固定特定位置，而不隨滾動欄滾動。

<div class="demo">
<div class="fixedSidebarGroup">
  <div class="sidebarList">
    <a href="#">
      <div class="listImg"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_grid2.svg" /></div>
      <div class="listTitle">側邊第一選項</div>
    </a>
  </div>
  <div class="sidebarList">
    <a href="#">
      <div class="listImg"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_setting2.svg" /></div>
      <div class="listTitle">側邊第二選項</div>
    </a>
  </div>
  <div class="sidebarList">
    <a href="#">
      <div class="listImg"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_home2.svg" /></div>
      <div class="listTitle">側邊第三選項</div>
    </a>
  </div>
  <div class="sidebarList">
    <a href="#">
      <div class="listImg"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_star2.svg" /></div>
      <div class="listTitle">側邊第四選項</div>
    </a>
  </div>
  <div class="sidebarList">
    <a href="#">
      <div class="listImg"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_heart2.svg" /></div>
      <div class="listTitle">側邊第五選項</div>
    </a>
  </div>
</div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="fixedSidebarGroup">
  <div class="sidebarList">
    <a href="#">
      <div class="listImg"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_grid2.svg" /></div>
      <div class="listTitle">側邊第一選項</div>
    </a>
  </div>
  <div class="sidebarList">
    <a href="#">
      <div class="listImg"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_setting2.svg" /></div>
      <div class="listTitle">側邊第二選項</div>
    </a>
  </div>
  <div class="sidebarList">
    <a href="#">
      <div class="listImg"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_home2.svg" /></div>
      <div class="listTitle">側邊第三選項</div>
    </a>
  </div>
  <div class="sidebarList">
    <a href="#">
      <div class="listImg"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_star2.svg" /></div>
      <div class="listTitle">側邊第四選項</div>
    </a>
  </div>
  <div class="sidebarList">
    <a href="#">
      <div class="listImg"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_heart2.svg" /></div>
      <div class="listTitle">側邊第五選項</div>
    </a>
  </div>
</div>
```

#### **CSS**

```sass
.fixedSidebarGroup {
  position: fixed;
  left: calc(100% - 45px);
  top: 10%;
  z-index: 99;
  .sidebarList {
    margin-bottom: 1px;
    display: block;
    position: relative;
    a {
      display: flex;
      white-space: nowrap;
      padding: 0 15px 0 0;
      color: #fff;
      align-items: center;
      min-width: 45px;
      min-height: 50px;
      overflow: hidden;
      width: 200px;
      transition: 0.5s;
      background-color: #0066cc;
      box-sizing: border-box;
      .listImg {
        margin: 10px;
        width: 25px;
        height: 25px;
        img {
          width: 25px;
          height: 25px;
        }
      }
      .listTitle {
        font-size: 0.938em;
      }
      &:hover,
      &:focus {
        background-color: darken(#0066cc, 20);
        transform: translateX(-155px);
        text-decoration: none;
      }
    }
  }
}

```

<!-- <iframe height="450" style="width: 100%;" scrolling="no" title="側邊選單01" src="https://codepen.io/u00hyui/embed/poPgOjZ?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/poPgOjZ">
  側邊選單01</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe> -->

<!-- tabs:end -->
<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<style>
  .demo{
   position: relative;
   margin:0 auto;
    overflow: hidden;
    width: 30%;
    height: 300px;
  }
.fixedSidebarGroup {
  position: absolute;
  left: calc(100% - 45px);
  top: 10%;
  z-index: 99;
}
.fixedSidebarGroup .sidebarList{
  margin-bottom: 1px;
  display: block;
  position: relative;
}
.fixedSidebarGroup .sidebarList a {
  display: flex;
  white-space: nowrap;
  padding: 0 15px 0 0;
  color: #fff;
  align-items: center;
  min-width: 45px;
  min-height: 50px;
  overflow: hidden;
  width: 200px;
  transition: 0.5s;
  background-color: #0066cc;
  box-sizing: border-box;
}
.fixedSidebarGroup .sidebarList a .listImg {
  margin: 10px;
  width: 25px;
  height: 25px;
}
.fixedSidebarGroup .sidebarList a .listImg img {
  width: 25px;
  height: 25px;
}
.fixedSidebarGroup .sidebarList a .list_title {
  font-size: 0.938em;
}
.fixedSidebarGroup .sidebarList a:hover, .fixedSidebarGroup .sidebarList a:focus {
  background-color: #003366;
  transform: translateX(-155px);
  text-decoration: none;
}
</style>
