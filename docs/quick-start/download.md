# 下載

從 **GitHub** 網站下載完整的 **hyUI kit** 原始程式碼。

?> 檔案下載連結 [GitHub 檔案下載](https://github.com/HywebU00/HyUI_v4.0)。

下載之後您會得到以下的檔案

- CSS 資料夾
- SASS 資料夾
- images 資料夾
- js 資料夾
- vendor 資料夾
- html 檔案
- README.md

?> 本框架需要具有編譯 **SASS/SCSS** 能力的開發人員使用。

## 檔案結構

```text

├── sass/
│   ├── page/
│   │   ├── _color.scss                 // color
│   │   ├── _cp.scss                    // cp
│   │   ├── _leftBlock.scss             // leftBlock
│   │   ├── _mp.scss                    // mp
│   │   ├── _sitemap.scss               // sitemap
│   │   └── _template.scss              // template
│   │
│   ├── sass/                           // scss所有檔案
│   │   ├── common/
│   │   ├── element/
│   │   ├── module/
│   │   └── ...
│   │
│   ├── _help.scss                      // 變數
│   ├── _variable.scss                  // 變數
│   └── style.scss                      // 統一匯出之主要SCSS
│
├── css/
│   └── style.css                       // sass輸出檔案
│
├── js/
│   ├── main.js                         // 壓縮 hyuijs   *勿更動
│   └── customize.js                    // 客製化js
│
├── vendor/
│   └── ...                             // 自行客製 或 載入plugin(ex:Swiper)
│
└─ images/
    ├── basic/                          // 基本預設圖檔
    ├── icon/                           // hyUI icon(svg)
    └── ...                             // 專案所需圖檔

```
