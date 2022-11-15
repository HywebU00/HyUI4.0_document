# SASS 架構

?>SASS 架構簡介：
全站的美容設計寶典。

## 架構內容

- <font >variable.scs 資全站樣式定義</font>
- <font >sass 資料夾</font>
- <font >page 資料夾</font>
- <font >style.scss 整合所有 scss</font>

<!-- 1. **<span class="focus">[\_variable.scss](#item-1):arrow_down:</span>**：全站樣式定義
2. **<span class="focus">[sass](#item-2):arrow_down:</span>**：模組
3. **<span class="focus">[page](#item-3):arrow_down:</span>**：特殊頁面
4. **<span class="focus">hyui.scss</span>**：將所需設定，從以上三項中 import 至 <span class="focus2">hyui.scss</span>，產出最終的 CSS -->

```text
├── sass/
   ├── page/
   │   ├── _color.scss                 // color
   │   ├── _cp.scss                    // cp
   │   ├── _leftBlock.scss             // leftBlock
   │   ├── _mp.scss                    // mp
   │   ├── _sitemap.scss               // sitemap
   │   └── _template.scss              // template
   │
   ├── sass/                           // scss所有檔案
   │   ├── common/
   │   ├── element/
   │   ├── module/
   │   └── ...
   │
   ├── _help.scss                      // ＠extend、@include使用參考
   ├── _variable.scss                  // 變數
   └── style.scss                      // 統一匯出之主要SCSS


```

## \_help.scss

可查詢常用的＠extend、@include 使用方式<

---

## \_variable.scss

:::warning
全站的基本定義，顏色、字型、格線系統
:::

<iframe height="265" style="width: 100%;" scrolling="no" title="_variable" src="https://codepen.io/Lize/embed/ExWaZXp?height=265&theme-id=dark&default-tab=css" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/Lize/pen/ExWaZXp'>_variable</a> by Lize wu
  (<a href='https://codepen.io/Lize'>@Lize</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

---

## style.scss

導入簡易的@layer 功能，讓實際撰寫內容不被原本 UI 架構影響。<br/>
只要在@layer webScss{} 之外的 scss 檔案權重都會比較高。<br/>
寫 CSS 可以減少使用!important 的用法，以及可以自行整理 css 而不被架構影響。

---

## sass

:::warning
分成三個資料夾：共通 common、 元件 element、 模組 module
:::

### 共通 common

- <span class="focus">mixins 資料夾：</span>基礎物件設定或算式，內含 extend、mixin 設定。
- <span class="focus">網頁基本設定：</span>mediaquery、格線系統 grid、reset、瀏覽器修正...等。

<div class="box">
<h3>附加說明</h3>
<ol>
    <li><span class="focus2">客製MIXIN</span> 引用 <span class="focus">mixins 資料夾</span> 內的設定，引用項目依需求而定。</li>
    <li><span class="focus2">_grid</span> 引用 <span class="focus">mixins 資料夾</span> 的 <span class="focus2">_flex-set.scss</span> 設定</li>
    <li>下圖列出結構以及比較常會使用的項目</li>
</ol>
</div>

<iframe style="border:none" width="100%" height="600" src="https://whimsical.com/embed/TnP7TaSjcRULShoTNjwQRs@VsSo8s35UvF22CfLJmd6x6"></iframe>

### 元件 element

- 文字、語言、按鈕、麵包屑...等，共 11 組元件。

<iframe style="border:none" width="100%" height="450" src="https://whimsical.com/embed/TnP7TaSjcRULShoTNjwQRs@2Ux7TurymQ8Sp7NQ2UTL"></iframe>

### 模組 module

- header、menu、固定側邊欄...等，目前共 18 個模組。

<iframe style="border:none" width="100%" height="450" src="https://whimsical.com/embed/TnP7TaSjcRULShoTNjwQRs@LUSUr8hW69X4QfGQB2"></iframe>

---

## page

:::warning
客制（mp）、固定應用（cp、sitemap...等）頁面。
<span class="focus2">\_template</span>為通用樣式，每個頁面如果要通用請寫在這邊
:::

<iframe style="border:none" width="100%" height="450" src="https://whimsical.com/embed/TnP7TaSjcRULShoTNjwQRs@LUSUr8hW5mgnK3teyH"></iframe>
