# Tooltip 提示框

?>檔案名稱：sass / element / `tooltip.scss`

### 項目的提示文字

表示小矩形快顯視窗 (Pop-Up Window)，它會在使用者將指標停留在控制項上時，顯示控制項用途的簡短說明。此用法不限用`div`、`span`、`em`、`a`...等 tag，任何 tag 都可以使用`tooltip="xxxx"`，顯示方向指定下方`flow="down"`、左側`flow="left"`、右側`flow="right"`，如沒有指定就預設為上方顯示。

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
</style>
