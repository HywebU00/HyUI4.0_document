# Language 選擇語系選單

?>檔案名稱：sass/element/`_language.scss`

此模組可單獨使用，語系數量不限，目前已預設用於`header`之`.navigation`區塊中，並已經自動設定偵測`html`裡面是否有`language`模組，讓`navigation`自動排版，讓模組放置於適當位置，如需要調整請參考以下設定。

<div class="language demo">
  <button>語言選擇</button>
  <ul>
    <li><a href="#">繁體中文</a></li>
    <li><a href="#">简体中文</a></li>
    <li><a href="#">ENGLISH</a></li>
  </ul>
</div>

## HTML 範本

```html
<div class="language">
  <button>語言選擇</button>
  <ul>
    <li><a href="#">繁體中文</a></li>
    <li><a href="#">简体中文</a></li>
    <li><a href="#">ENGLISH</a></li>
  </ul>
</div>
```

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4/css/style.css" />
<style>
.language button {
  width: 150px;
}
.demo{
  margin:4rem 0;
}
</style>
