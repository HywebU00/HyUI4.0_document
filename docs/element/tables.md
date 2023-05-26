# Table / 表格

?>檔案名稱：sass / module / `_table.scss`

---

## 基本表格樣式

<!-- panels:start -->

<table>
 <caption>
  無障礙表格標題
 </caption>
  <thead>
    <tr>
      <th>編號</th>
      <th>姓名</th>
      <th>性別</th>
      <th>年齡</th>
      <th>居住地</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>王大明</td>
      <td>男</td>
      <td>39</td>
      <td>台北市</td>
    </tr>
    <tr>
      <td>2</td>
      <td>李小強</td>
      <td>男</td>
      <td>25</td>
      <td>宜蘭縣</td>
    </tr>
    <tr>
      <td>3</td>
      <td>林珍珍</td>
      <td>女</td>
      <td>33</td>
      <td>新竹市</td>
    </tr>
  </tbody>
</table>

<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
<table>
  <caption>
    障礙表格標題
    <!-- 若表格內容複雜，可以補充摘要(summary)來加強說明表格內容，但 內容不要與標題重複 -->
    <!-- <span class="summary">表格摘要</span> -->
  </caption>
  <thead>
    <tr>
      <th>...</th>
      <th>...</th>
      <th>...</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>...</td>
    </tr>
    <tr>
      <td>...</td>
    </tr>
  </tbody>
</table>
```

<!-- tabs:end -->

### td 有 hover 效果

table 加上`tableHover`的 className

<!-- panels:start -->
<table class="tableHover">
 <caption>
    表格有Hover效果
    <!-- 若表格內容複雜，可以補充摘要(summary)來加強說明表格內容，但 內容不要與標題重複 -->
    <!-- <span class="summary">表格摘要</span> -->
  </caption>
  <thead>
    <tr>
      <th>編號</th>
      <th>姓名</th>
      <th>性別</th>
      <th>年齡</th>
      <th>居住地</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>王大明</td>
      <td>男</td>
      <td>39</td>
      <td>台北市</td>
    </tr>
    <tr>
      <td>2</td>
      <td>李小強</td>
      <td>男</td>
      <td>25</td>
      <td>宜蘭縣</td>
    </tr>
    <tr>
      <td>3</td>
      <td>林珍珍</td>
      <td>女</td>
      <td>33</td>
      <td>新竹市</td>
    </tr>
  </tbody>
</table>
<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
<table class="tableHover"></table>
```

<!-- tabs:end -->

### td 有間隔不同背景色

table 加上`table_sprite`的 className

<!-- panels:start -->
<table class="tableSprite">
<caption>
    td間隔不同背景色
  </caption>
    <thead>
        <tr>
            <th>編號</th>
            <th>姓名</th>
            <th>性別</th>
            <th>年齡</th>
            <th>居住地</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>王大明</td>
            <td>男</td>
            <td>39</td>
            <td>台北市</td>
        </tr>
        <tr>
            <td>2</td>
            <td>李小強</td>
            <td>男</td>
            <td>25</td>
            <td>宜蘭縣</td>
        </tr>
        <tr>
            <td>3</td>
            <td>林珍珍</td>
            <td>女</td>
            <td>33</td>
            <td>新竹市</td>
        </tr>
        <tr>
            <td>4</td>
            <td>黃志明</td>
            <td>男</td>
            <td>44</td>
            <td>台南市</td>
        </tr>
        <tr>
            <td>5</td>
            <td>郭春嬌</td>
            <td>女</td>
            <td>37</td>
            <td>台中市</td>
        </tr>
    </tbody>
</table>
<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
<table class="tableSprite"></table>
```

<!-- tabs:end -->

## 響應式排版表格

支援響應式條列式重新排版表格

使用`before`取代`th`，在`table`上一層使用`<div class="tableList"></div>`將`table`包覆住，即可於手機版重新排版表格樣式。

<!-- panels:start -->
<div class="tableList">
    <table>
        <thead>
            <tr>
                <th>編號</th>
                <th>據點</th>
                <th>地址</th>
                <th>電話</th>
                <th>傳真</th>
                <th>信箱</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>01</td>
                <td>總公司</td>
                <td>新竹縣竹北市台元一街8號5樓之6</td>
                <td>02-12345678</td>
                <td>02-12345678</td>
                <td><a href="#"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_mail.svg" alt=""></a></td>
            </tr>
            <tr>
                <td>02</td>
                <td>臺北分公司</td>
                <td>臺北市重慶南路二段51號5樓</td>
                <td>02-12345678</td>
                <td>02-12345678</td>
                <td><a href="#"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_mail.svg" alt=""></a></td>
            </tr>
            <tr>
                <td>03</td>
                <td>臺中分公司</td>
                <td>臺中市西屯區臺灣大道三段658號6樓A1</td>
                <td>02-12345678</td>
                <td>02-12345678</td>
                <td><a href="#"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_mail.svg" alt=""></a></td>
            </tr>
            <tr>
                <td>04</td>
                <td>高雄分公司</td>
                <td>高雄市新興區中正三路55號26樓之5</td>
                <td>02-12345678</td>
                <td>02-12345678</td>
                <td><a href="#"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_mail.svg" alt=""></a></td>
            </tr>
            <tr>
                <td>05</td>
                <td>曼谷分公司</td>
                <td>Room No.2009, 20th F1., Le Concorde Tower, 202 Ratchadapisek Rd., Huaykwang, Bangkok 10310</td>
                <td>02-12345678</td>
                <td>02-12345678</td>
                <td><a href="#"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_mail.svg" alt=""></a></td>
            </tr>
            <tr>
                <td>06</td>
                <td>北京</td>
                <td>北京市海淀区安宁庄西路9号院29号楼金泰富地大厦105室</td>
                <td>02-12345678</td>
                <td>02-12345678</td>
                <td><a href="#"><img src="https://hywebu00.github.io/hyui_flex/images/icon/icon_mail.svg" alt=""></a></td>
            </tr>
        </tbody>
    </table>
</div>
<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
<div class="tableList">
  <table>
    <caption>
      障礙表格標題
      <!-- 若表格內容複雜，可以補充摘要(summary)來加強說明表格內容，但 內容不要與標題重複 -->
      <!-- <span class="summary">表格摘要</span> -->
    </caption>
    <thead>
      <tr>
        <th>...</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>...</td>
      </tr>
      <tr>
        <td>...</td>
      </tr>
      <tr>
        <td>...</td>
      </tr>
    </tbody>
  </table>
</div>
```

#### **JavaScript**

```javascript
//在 table 增加 data-* 標籤
function tableAddDataAttributes(obj) {
  const el = document.querySelectorAll(obj.elemClass);
  function setTrAttr(i) {
    const thList = i.querySelectorAll('th');
    const trList = i.querySelectorAll('tr');
    trList.forEach((trItem) => {
      const tdList = trItem.querySelectorAll('td');
      tdList.forEach((i, idx) => {
        tdList[idx].setAttribute(`data-${obj.dataName}`, `${thList[idx].textContent}`);
      });
    });
  }
  el.forEach((i) => {
    const tableItem = i.querySelectorAll('table');
    tableItem.forEach((i) => {
      setTrAttr(i);
    });
  });
}

tableAddDataAttributes({
  elemClass: '.tableList', // 目標table
  dataName: 'title', // tableList樣式 加上 data-title
});
```

<!-- tabs:end -->

## 固定左側表頭

固定左邊表頭，資料可水平捲動

適用於左側有`th`的資料，在手機版可做成固定`th`，其餘 `td` 可橫向水平捲動，在`table`最外層請用`fixThTable`包覆。

<!-- panels:start -->
<div class="fixThTable">
    <table>
        <tr>
            <th>th 1</th>
            <th>th 2</th>
            <th>th 3</th>
            <th>th 4</th>
            <th>th 5</th>
            <th>th 6</th>
        </tr>
        <tr>
            <th>th A</th>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
        </tr>
        <tr>
            <th>th B</th>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
        </tr>
        <tr>
            <th>th C</th>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
            <td>td 資料</td>
        </tr>
    </table>
</div>
<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
<div class="fixThTable">
  <caption>
    障礙表格標題
    <!-- 若表格內容複雜，可以補充摘要(summary)來加強說明表格內容，但 內容不要與標題重複 -->
    <!-- <span class="summary">表格摘要</span> -->
  </caption>
  <table>
    <tr>
      <th>th 1</th>
      <th>th 2</th>
      <th>th 3</th>
      <th>th 4</th>
      <th>th 5</th>
      <th>th 6</th>
    </tr>
    <tr>
      <th>th A</th>
      <td>td 資料</td>
      <td>td 資料</td>
      <td>td 資料</td>
      <td>td 資料</td>
      <td>td 資料</td>
    </tr>
    <tr>
      <th>th B</th>
      <td>td 資料</td>
      <td>td 資料</td>
      <td>td 資料</td>
      <td>td 資料</td>
      <td>td 資料</td>
    </tr>
    <tr>
      <th>th C</th>
      <td>td 資料</td>
      <td>td 資料</td>
      <td>td 資料</td>
      <td>td 資料</td>
      <td>td 資料</td>
    </tr>
  </table>
</div>
```

<!-- tabs:end -->

## Scroll 表格設定

> 按照專案經驗，在客戶資料上稿常常出現表格會撐出畫面或是破圖的情況，這部分可以使用預設提供之 JavaScript 設定，讓文章內容頁面的表格自動產生響應式橫向捲軸，以防止畫面跑版。<br/>
> 若要表格能夠左右滾動 則須在最外層增加 `tableWrapper`的 className
> 在 `table` 同層 增加 `scrollTable`的 className

<!-- panels:start -->
<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
<!-- 如果要能夠左右滾動 則須在最外層增加 class “tableWrapper”
  在table同層 增加 class "scrolTable" -->
<div class="tableWrapper">
  <table class="scrollTable ">
    <caption>
      無障礙表格標題可以srcoll
      <!-- 若表格內容複雜，可以補充摘要(summary)來加強說明表格內容，但 內容不要與標題重複 -->
    </caption>
    <thead>
      <tr>
        <th>...</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>...</td>
      </tr>
      <tr>
        <td>...</td>
      </tr>
      <tr>
        <td>...</td>
      </tr>
    </tbody>
  </table>
</div>
```

#### **JavaScript**

```javascript
function scrollTables(obj) {
  let el = document.querySelectorAll(obj) || null; // --- 按鈕列表名稱

  // --- 檢查父層有沒有 tableList
  function appendEle() {
    el.forEach((i) => {
      let _appendLeftEle;
      let _appendRightEle;
      let _leftBtn;
      let _rightBtn;
      let _hasItem = i.parentElement.classList.contains('tableList');
      let _hasNavLeft = i.parentElement.querySelector('.scrollTableNavLeft');
      if (!_hasItem && _hasNavLeft === null) {
        _appendLeftEle = document.createElement('div');
        _appendLeftEle.setAttribute('class', 'scrollTableNav scrollTableNavLeft');
        _appendLeftEle.style.height = `${i.parentElement.clientHeight}px`;
        _appendRightEle = document.createElement('div');
        _appendRightEle.setAttribute('class', 'scrollTableNav scrollTableNavRight');
        _appendRightEle.style.height = `${i.parentElement.clientHeight}px`;
        i.parentElement.style.position = 'relative';
        i.parentElement.prepend(_appendLeftEle, _appendRightEle);
        // --- 增加左邊按鈕
        _leftBtn = document.createElement('div');
        _leftBtn.setAttribute('class', 'scrollTableLeftBtn');
        _appendLeftEle.appendChild(_leftBtn);
        // --- 增加右邊按鈕
        _rightBtn = document.createElement('div');
        _rightBtn.setAttribute('class', 'scrollTableRightBtn');
        _appendRightEle.appendChild(_rightBtn);
        displayNoneEle();
      }
    });
  }

  // --- 開關遮罩功能
  function displayNoneEle() {
    el.forEach((i) => {
      let _hasItem = i.parentElement.classList.contains('tableList');
      if (!_hasItem) {
        hiddenEle(i);
      }
      function hiddenEle(el) {
        // --- 父層元素的寬;
        let _table = el.parentElement.clientWidth;
        // --- 子層元素的寬
        let _tableItem = el.scrollWidth;
        // --- 左邊遮罩
        let _rightEle = el.parentElement.querySelector('.scrollTableNavRight');
        // --- 右邊遮罩
        let _leftEle = el.parentElement.querySelector('.scrollTableNavLeft');
        // --- 如果沒有建立遮罩
        if (_rightEle == null) {
          return;
        }
        // --- 如果子層跟父層一樣寬度
        if (_table === _tableItem) {
          _leftEle.style.display = 'none';
          _rightEle.style.display = 'none';
        } else {
          el.parentElement.scrollLeft = '0';
          _rightEle.style.display = 'block';
          _rightEle.style.opacity = '1';
        }
        eleScroll();
      }
    });
  }
  // --- 當父層滾輪滾動
  function eleScroll() {
    el.forEach((i) => {
      i.parentElement.addEventListener('scroll', () => {
        // --- 父層元素的寬
        let _table = i.parentElement.clientWidth;
        // --- 子層元素的寬
        let _tableItem = i.scrollWidth;
        // --- 左邊遮罩
        let _rightEle = i.parentElement.querySelector('.scrollTableNavRight');
        // --- 右邊遮罩
        let _leftEle = i.parentElement.querySelector('.scrollTableNavLeft');
        // --- 捲軸位置
        let _scrollPosition = i.parentElement.scrollLeft;
        _rightEle.style.right = `-${i.parentElement.scrollLeft}px`;
        _leftEle.style.left = `${i.parentElement.scrollLeft}px`;

        if (_scrollPosition === 0) {
          _leftEle.style.opacity = 0;
          _rightEle.style.opacity = 1;
        }
        // --- 如果捲軸位置還沒到底
        if (_scrollPosition > 0) {
          _leftEle.style.opacity = 1;
        }
        // --- 如果捲軸位置＋父層寬度 ＝ 子層寬度
        if (_scrollPosition + _table === _tableItem) {
          _rightEle.style.opacity = 0;
          _leftEle.style.opacity = 1;
          _leftEle.style.display = 'block';
        }
        // --- 如果捲軸位置＋父層寬度 < 子層寬度
        if (_scrollPosition + _table < _tableItem) {
          _rightEle.style.opacity = 1;
        }
      });
    });
  }

  // --- 點擊左右按鈕時滾動畫面
  function clickEleBtn() {
    // --- 點擊左邊按鈕
    const leftBtn = document.querySelectorAll('.scrollTableLeftBtn');
    if (leftBtn.length !== 0) {
      leftBtn.forEach((i) => {
        i.addEventListener('click', (item) => {
          i.parentElement.parentElement.scrollLeft -= 200;
        });
      });
    }
    // --- 點擊右邊按鈕
    const rightBtn = document.querySelectorAll('.scrollTableRightBtn');
    if (rightBtn.length !== 0) {
      rightBtn.forEach((i) => {
        i.addEventListener('click', (item) => {
          i.parentElement.parentElement.scrollLeft += 200;
        });
      });
    }
  }

  appendEle();
  clickEleBtn();
  // --- resize
  window.addEventListener('resize', () => {
    let _hasItem;
    el.forEach((i) => {
      _hasItem = i.parentElement.classList.contains('tableList');
      if (!_hasItem) {
        displayNoneEle();
      }
    });
  });
}
scrollTables('table'); // table捲動功能
```

<!-- tabs:end -->

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4/css/style.css" />
<style>
/* 取消 markdown 預設狀態 */
.markdown-section p.tip, .markdown-section tr:nth-child(2n) {
    background-color:unset;
}
.markdown-section table{
  display:table;
}
@media screen and (max-width: 575px){
  .markdown-section td{
    padding-left: 0.5em !important;
    padding-top: 2em;
}
}
table{
  margin:4em 0 !important;
}
table caption{
  text-align: center;
}
table.tableHover tr:hover {
    background: #f3f3f3 !important;
}
table.tableSprite tr:nth-child(even) {
    background: #f5f5f5 !important;
}
td img{
   max-width: 20px !important;
}
.fixThTable table{
  display:block;
}
.fixThTable td,.fixThTable th{
padding: 0.8em 0;
}
</style>
<script>
  function tableAddDataAttributes(obj) {
  const el = document.querySelectorAll(obj.elemClass);
  function setTrAttr(i) {
    const thList = i.querySelectorAll('th');
    const trList = i.querySelectorAll('tr');
    trList.forEach((trItem) => {
      const tdList = trItem.querySelectorAll('td');
      tdList.forEach((i, idx) => {
        tdList[idx].setAttribute(`data-${obj.dataName}`, `${thList[idx].textContent}`);
      });
    });
  }
  el.forEach((i) => {
    const tableItem = i.querySelectorAll('table');
    tableItem.forEach((i) => {
      setTrAttr(i);
    });
  });
}
tableAddDataAttributes({
  elemClass: '.tableList', // 目標table
  dataName: 'title', // tableList樣式 加上 data-title
});
</script>
