# Tooltip 提示框

?>檔案名稱：sass / element / `tooltip.scss`

### 項目的提示文字

表示 **小矩形快顯視窗** (Pop-Up Window) ，它會在使用者將指標停留在控制項上時，顯示控制項用途的簡短說明。此用法不限用`div`、`span`、`em`、`a`...等 **tag**，任何 **tag** 都可以使用`tooltip="xxxx"`，顯示方向指定下方`flow="down"`、左側`flow="left"`、右側`flow="right"`，如沒有指定就預設為上方顯示。

<!-- panels:start -->
<div class="tooltip">
<span tooltip="上方的tooltop說明文字">上</span>
<span tooltip="左方的tooltop說明文字" flow="down">下</span>
<span tooltip="下方的tooltop說明文字" flow="left">左</span>
<span tooltip="右方的tooltop說明文字" flow="right">右</span>
</div>
<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
<span tooltip="上方的tooltop說明文字">上</span>
<span tooltip="左方的tooltop說明文字" flow="down">下</span>
<span tooltip="下方的tooltop說明文字" flow="left">左</span>
<span tooltip="右方的tooltop說明文字" flow="right">右</span>
```

<!-- tabs:end -->

### 文章的提示文字

文章內容內也可以加入`tooltip`

<!-- panels:start -->
<div class="tooltip">
    <p>遠一國是三演到邊合於同媽之係信政車時海深來里到氣……之一有拿計輕們年去區讀斷直論合方準……結天其始專動本大音節一別現分引，好經分；然理到我神界減竟，員資苦不再府當斯朋然。</p>
    <p>最病行狀什記。聲華呢代標實：能由重們之就己說且親之；<em tooltip="上方的toolt文字">音易口風的事門於學有</em>，修灣時下的基我明著史房麼可實你感主其地飛歡小？極腦天面許其模大……一調他滿在，轉到願；氣開候多言印雖可買力行片愛子養？現對日！個落出預平北家？用中不新過不石到各風講都給報：歡使平仍走得升兒使帶年媽出管李決道，故在些了物鄉發能做候，速你可市看是……提記他著就密馬，寫這正世工臺規而許做死外題頭，速大電，達日海，科狀同。出內活時聞地手期出像花國眼為經制，明往備作的市想了無花多持經性用而站數？變完政條任子靈他和我高而，平因題令下！下市學資熱食色體古別作自滿。</p>
</div>
<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
....xxxx<em tooltip="上方的tooltop說明文字">音易口風的事門於學有</em>xxxx....
```

<!-- tabs:end -->

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<style>
.tooltip {
    margin:4em 0;
}
    .tooltip span {
    display: inline-block;
    background: #DEDEDE;
    text-align: center;
    padding: 10px;
    width: 100px;
    line-height: 20px;
    vertical-align: baseline;
}
.tooltip em{
    color:red;
}
.tooltip p{
        text-align: start;
}
.tooltip{
    padding: 10px 0;
}
[tooltip] {
    position: relative;
  }
  em[tooltip] {
    text-decoration: none;
    color: #00a4f9;
  }
  em[tooltip]:hover, em[tooltip]:focus-visible {
    color: #0094e0;
    cursor: pointer;
  }
  em[tooltip]:focus-visible {
    outline: #1aadfa 2px solid;
  }
  [tooltip]:before,
[tooltip]:after {
    text-transform: none;
    -webkit-user-select: none;
       -moz-user-select: none;
        -ms-user-select: none;
            user-select: none;
    pointer-events: none;
    position: absolute;
    display: none;
    opacity: 0;
  }
  [tooltip]:before {
    content: "";
    border: 5px solid transparent;
    z-index: 1001;
  }
  [tooltip]:after {
    content: attr(tooltip);
    text-align: left;
    min-width: 150px;
    line-height: 1.5em;
    max-width: 300px;
    font-size: 0.813em;
    max-height: 5.182875em;
    overflow: hidden;
    padding: 0.5em;
    border-radius: 4px;
    box-shadow: 0 1em 2em -0.5em rgba(0, 0, 0, 0.35);
    background: #333;
    color: #fff;
    z-index: 1000;
    box-sizing: border-box;
  }
  [tooltip]:hover:before,
[tooltip]:hover:after {
    display: block;
  }
  [tooltip=""]:before,
[tooltip=""]:after {
    display: none !important;
  }
  [tooltip]:not([flow]):before,
[tooltip][flow^=up]:before {
    bottom: 100%;
    border-bottom-width: 0;
    border-top-color: #333;
  }
  [tooltip]:not([flow]):after,
[tooltip][flow^=up]:after {
    bottom: calc(100% + 5px);
  }
  [tooltip]:not([flow]):before,
[tooltip]:not([flow]):after,
[tooltip][flow^=up]:before,
[tooltip][flow^=up]:after {
    left: 50%;
    transform: translate(-50%, -0.5em);
  }
  [tooltip][flow^=down]:before {
    top: 100%;
    border-top-width: 0;
    border-bottom-color: #333;
  }
  [tooltip][flow^=down]:after {
    top: calc(100% + 5px);
  }
  [tooltip][flow^=down]:before,
[tooltip][flow^=down]:after {
    left: 50%;
    transform: translate(-50%, 0.5em);
  }
  [tooltip][flow^=left]:before {
    top: 50%;
    border-right-width: 0;
    border-left-color: #333;
    left: calc(0em - 5px);
    transform: translate(-0.5em, -50%);
  }
  [tooltip][flow^=left]:after {
    top: 50%;
    right: calc(100% + 5px);
    transform: translate(-0.5em, -50%);
  }
  [tooltip][flow^=right]:before {
    top: 50%;
    border-left-width: 0;
    border-right-color: #333;
    right: calc(0em - 5px);
    transform: translate(0.5em, -50%);
  }
  [tooltip][flow^=right]:after {
    top: 50%;
    left: calc(100% + 5px);
    transform: translate(0.5em, -50%);
  }
  @-webkit-keyframes tooltips-vert {
    to {
      opacity: 0.9;
      transform: translate(-50%, 0);
    }
  }
  @keyframes tooltips-vert {
    to {
      opacity: 0.9;
      transform: translate(-50%, 0);
    }
  }
  @-webkit-keyframes tooltips-horz {
    to {
      opacity: 0.9;
      transform: translate(0, -50%);
    }
  }
  @keyframes tooltips-horz {
    to {
      opacity: 0.9;
      transform: translate(0, -50%);
    }
  }
  /* FX All The Things */
  [tooltip]:not([flow]):hover:before,
[tooltip]:not([flow]):hover:after,
[tooltip][flow^=up]:hover:before,
[tooltip][flow^=up]:hover:after,
[tooltip][flow^=down]:hover:before,
[tooltip][flow^=down]:hover:after {
    -webkit-animation: tooltips-vert 300ms ease-out forwards;
            animation: tooltips-vert 300ms ease-out forwards;
  }
  [tooltip][flow^=left]:hover:before,
[tooltip][flow^=left]:hover:after,
[tooltip][flow^=right]:hover:before,
[tooltip][flow^=right]:hover:after {
    -webkit-animation: tooltips-horz 300ms ease-out forwards;
            animation: tooltips-horz 300ms ease-out forwards;
  }
  .tooltip {
    text-align: center;
    padding: 40px 0;
  }
  .tooltip span {
    display: inline-block;
    background: #dedede;
    text-align: center;
    padding: 10px;
    width: 100px;
    line-height: 20px;
    vertical-align: baseline;
  }
  .tooltip p > em {
    color: red;
  }
</style>
