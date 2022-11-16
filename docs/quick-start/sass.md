# SASS 架構

?>SASS 架構簡介：
全站的美容設計寶典。

## 架構內容

- variable.scs 資全站樣式定義
- sass 資料夾
- page 資料夾
- style.scss 整合所有 scss

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

可查詢常用的 **＠extend**、 **@include** 使用方式

---

## \_variable.scss

全站的 **基本定義**，**顏色**、**字型**、**格線系統**

```sass
// 定義顏色 此顏色可自由變換
$colorPrimary: #00a4f9; //主色
$colorSecondary: #781f79; //輔色
$colorLight: #fec003; //點綴
$colorLink: #00a4f9; //連結
$colorImportant: #eb0202; //重要
// 但注意真實顏色與語意的關聯必須易於辨識
$colorBlue: #0066cc;
$colorGreen: #298729;
$colorOrange: #d04500;
$colorRed: #d30000;
$colorYellow: #fec003;
$colorPurple: #781f79;
$colorGray: #ccc;
$colorDark: #333333;
$colorHr: #666; //hr顏色
$colorWord: #222; //一般字的顏色
$btnWordColor: #222; //按鈕字的顏色
// 連結顏色
$aColor: #00a4f9;
$aHover: mix($aColor, #000, 90%);
$aFocus: mix($aColor, #fff, 90%);
// 表單focus顏色
$formFocus: #00a4f9; //表單
$form-btn: #00a4f9; //表單
// 按鈕設定
$btn-border: mix($btnWordColor, #000, 10%);
$btnPadding: 0.5em 1.25em;
$btnRadius: 0.2em;
$btnBg: #e0e0e0;

//------------------------------------------------------字型--------//

// 字型設定
$fontFamily: Lato, 'PingFang TC', 'Helvetica Neue', Helvetica, 微軟正黑體, Arial, sans-serif;

$fontSize: 1em;

// rem基本尺寸
$remFontSize: 16;

//------------------------------------------------------格線系統-----//

// 格線系統
$gridColumns: 12 !default; //格線欄位數
$gridGutterWidth: 30px !default; //左右padding
$containerMax: 1200px !default; //container最大寬

//mediaquery
$screenLg: 1400px !default; //電腦
$screenMd: 992px !default; //平板
$screenSm: 768px !default; //手機
$screenXs: 576px !default; //極小尺寸 - hyui
$screenXs-flex: 320px !default; //極小尺寸 - flex

//-------------------------------------------------------sitemap------//

$sitemapLength: 4;
$sitemapWidth: calc(100% / $sitemapLength);

//-------------------------------------------------------表單------//

$formTitleWidth: 150px; // 表單title寬度

//-------------------------------------------------------functionPanel------//

$colorFunction: #666;

//-------------------------------------------------------手機版選單------//

$colorSidebarBg: saturate(darken($colorPrimary, 18), 20);
// 選色參考：https://sassme.jim-nielsen.com/
$menuItems: 15;

//-------------------------------------------------------footer------//

$fatFooterBgColor: #f1f1f1; //fatFooter 底色

//--------------------------------------------------------客製化------//

$roundedAngle: 10px; //整站導角
$cubic: cubic-bezier(0.4, 0.01, 0.165, 0.99); //動態預設

```

<!-- <iframe height="265" style="width: 100%;" scrolling="no" title="_variable" src="https://codepen.io/Lize/embed/ExWaZXp?height=265&theme-id=dark&default-tab=css" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/Lize/pen/ExWaZXp'>_variable</a> by Lize wu
  (<a href='https://codepen.io/Lize'>@Lize</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe> -->

---

## style.scss

導入簡易的 **@layer** 功能，讓實際撰寫內容不被原本 UI 架構影響。<br/>
只要在 **@layer** **webScss{}** 之外的 **scss** 檔案權重都會比較高。<br/>
寫 CSS 可以減少使用 **!important** 的用法，以及可以自行整理 **css** 而不被架構影響。

## sass

分成三個資料夾：**共通 common**、 **元件 element**、 **模組 module**

### 共通 common

- **mixins** **資料夾：**基礎物件設定或算式，內含 **extend**、**mixin** 設定。
- **網頁基本設定：** mediaquery、格線系統 grid、reset、瀏覽器修正...等。

?>**附加說明**<br>1. 客製 MIXIN<引用 mixins 資料夾內的設定，引用項目依需求而定。<br> 2.**grid** 引用 **mixins** 資料夾 的 **\_flex-set.scss 設定**<br> 3.下圖列出結構以及比較常會使用的項目

<iframe style="border:none" width="100%" height="600" src="https://whimsical.com/embed/TnP7TaSjcRULShoTNjwQRs@VsSo8s35UvF22CfLJmd6x6"></iframe>

### 元件 element

- 文字、語言、按鈕、麵包屑...等，共 11 組元件。

<iframe style="border:none" width="100%" height="450" src="https://whimsical.com/embed/TnP7TaSjcRULShoTNjwQRs@2Ux7TurymQ8Sp7NQ2UTL"></iframe>

### 模組 module

- header、menu、固定側邊欄...等，目前共 18 個模組。

<iframe style="border:none" width="100%" height="450" src="https://whimsical.com/embed/TnP7TaSjcRULShoTNjwQRs@LUSUr8hW69X4QfGQB2"></iframe>

---

## page

客制（mp）、固定應用（cp、sitemap...等）頁面。
**\_template** 為通用樣式，每個頁面如果要通用請寫在這邊

<iframe style="border:none" width="100%" height="450" src="https://whimsical.com/embed/TnP7TaSjcRULShoTNjwQRs@LUSUr8hW5mgnK3teyH"></iframe>
