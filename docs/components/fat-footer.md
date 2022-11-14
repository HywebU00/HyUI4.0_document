# Fat-footer / 頁尾選單

?>檔案名稱：sass/ module / `fatfooter.scss`

 <section class="fatFooter">
        <div class="container">
          <button type="button" name="展開選單/OPEN" aria-label="導覽選單展開/收合" class="btn btnFatFooter">收合</button>
          <nav>
            <ul>
              <li>
                <a href="#">關於本局</a>
                <ul>
                  <li><a href="#">本局沿革</a></li>
                  <li><a href="#">本局願景</a></li>
                  <li><a href="#">組織介紹</a></li>
                  <li><a href="#">本局願景</a></li>
                  <li><a href="#">局處執掌</a></li>
                  <li><a href="#">重大政策</a></li>
                  <li><a href="#">施政重點</a></li>
                  <li><a href="#">本局位置</a></li>
                </ul>
              </li>
              <li>
                <a href="#">訊息公告</a>
                <ul>
                  <li><a href="#">本局公告</a></li>
                  <li><a href="#">環保署公告</a></li>
                  <li><a href="#">環境用藥公告</a></li>
                  <li><a href="#">環保專案成果報告</a></li>
                </ul>
              </li>
              <li>
                <a href="#">業務專區</a>
                <ul>
                  <li><a href="#">化學物質</a></li>
                  <li><a href="#">毒性化學物質</a></li>
                  <li><a href="#">危害性化學物質災害防救</a></li>
                  <li><a href="#">環境用藥</a></li>
                  <li><a href="#">石綿危害資訊</a></li>
                </ul>
              </li>
              <li>
                <a href="#">便民服務</a>
                <ul>
                  <li><a href="#">線上服務</a></li>
                  <li><a href="#">教育宣導</a></li>
                  <li><a href="#">影音專區</a></li>
                  <li><a href="#">下載專區</a></li>
                  <li><a href="#">常見問答</a></li>
                  <li><a href="#">相關連結</a></li>
                  <li><a href="#">訂閱電子報</a></li>
                </ul>
              </li>
              <li>
                <a href="#">政府資訊公開</a>
                <ul>
                  <li><a href="#">行政院環境保護署資訊公開要點</a></li>
                  <li><a href="#">預算及會計月報</a></li>
                  <li><a href="#">性別平等專區</a></li>
                  <li><a href="#">人權專區</a></li>
                  <li><a href="#">環境統計資料庫</a></li>
                  <li><a href="#">業務標準作業流程</a></li>
                  <li><a href="#">行政院環保署Open Data資料集</a></li>
                </ul>
              </li>
              <li>
                <a href="#">法規專區</a>
                <ul>
                  <li><a href="#">主管法規查詢系統</a></li>
                  <li><a href="#">全國法規資料庫</a></li>
                </ul>
              </li>
            </ul>
          </nav>
        </div>
      </section>

<!-- tabs:start -->

#### **HTML**

```html
<section class="fatFooter">
  <div class="container">
    <button type="button" name="展開選單/OPEN" aria-label="導覽選單展開/收合" class="btn btnFatFooter">收合</button>
    <nav>
      <ul>
        <li>
          <a href="#">關於本局</a>
          <ul>
            <li><a href="#">本局沿革</a></li>
            <li><a href="#">本局願景</a></li>
            <li><a href="#">組織介紹</a></li>
            <li><a href="#">本局願景</a></li>
            <li><a href="#">局處執掌</a></li>
            <li><a href="#">重大政策</a></li>
            <li><a href="#">施政重點</a></li>
            <li><a href="#">本局位置</a></li>
          </ul>
        </li>
        <li>
          <a href="#">訊息公告</a>
          <ul>
            <li><a href="#">本局公告</a></li>
            <li><a href="#">環保署公告</a></li>
            <li><a href="#">環境用藥公告</a></li>
            <li><a href="#">環保專案成果報告</a></li>
          </ul>
        </li>
        <li>
          <a href="#">業務專區</a>
          <ul>
            <li><a href="#">化學物質</a></li>
            <li><a href="#">毒性化學物質</a></li>
            <li><a href="#">危害性化學物質災害防救</a></li>
            <li><a href="#">環境用藥</a></li>
            <li><a href="#">石綿危害資訊</a></li>
          </ul>
        </li>
        <li>
          <a href="#">便民服務</a>
          <ul>
            <li><a href="#">線上服務</a></li>
            <li><a href="#">教育宣導</a></li>
            <li><a href="#">影音專區</a></li>
            <li><a href="#">下載專區</a></li>
            <li><a href="#">常見問答</a></li>
            <li><a href="#">相關連結</a></li>
            <li><a href="#">訂閱電子報</a></li>
          </ul>
        </li>
        <li>
          <a href="#">政府資訊公開</a>
          <ul>
            <li><a href="#">行政院環境保護署資訊公開要點</a></li>
            <li><a href="#">預算及會計月報</a></li>
            <li><a href="#">性別平等專區</a></li>
            <li><a href="#">人權專區</a></li>
            <li><a href="#">環境統計資料庫</a></li>
            <li><a href="#">業務標準作業流程</a></li>
            <li><a href="#">行政院環保署Open Data資料集</a></li>
          </ul>
        </li>
        <li>
          <a href="#">法規專區</a>
          <ul>
            <li><a href="#">主管法規查詢系統</a></li>
            <li><a href="#">全國法規資料庫</a></li>
          </ul>
        </li>
      </ul>
    </nav>
  </div>
</section>
```

#### **JavaScript**

```javascript
function fatFooter(obj) {
  const el = document.querySelector('.btnFatFooter') || null; // --- 控制的對象
  const fontBtn = document.querySelectorAll('.fontSize ul li a');
  function fatFooterInit() {
    // --- 抓取UI高度 css樣式修改樣式重新抓取高度
    const _navUl = el.parentNode.querySelectorAll('nav ul li ul');
    setTimeout(() => {
      _navUl.forEach((i) => {
        i.setAttribute('style', '');
        let _itemHeight = i.offsetHeight;
        i.dataset.itemHeight = _itemHeight;
        if (Number(_itemHeight) !== 0) {
          i.style.height = `${Number(i.dataset.itemHeight)}px`;
        } else {
          i.style.height = '0px';
        }
      });
    }, 20);
  }
  function toggleFatFooter() {
    const _navUl = el.parentNode.querySelectorAll('nav ul li ul');
    _navUl.forEach((i) => {
      if (i.offsetHeight !== 0) {
        i.style.height = '0px';
        el.innerHTML = '收合/CLOSE';
        el.setAttribute('name', '收合選單/CLOSE');
      } else {
        i.style.height = `${i.dataset.itemHeight}px`;
        el.innerHTML = '展開/OPEN';
        el.setAttribute('name', '展開選單/OPEN');
      }
    });
    el.classList.toggle('close');
  }
  fatFooterInit();
  // --- 點擊時
  el.addEventListener('click', toggleFatFooterEle);
  function toggleFatFooterEle() {
    setTimeout(() => {
      el.addEventListener('click', toggleFatFooterEle);
    }, 500);
    el.removeEventListener('click', toggleFatFooterEle);
    toggleFatFooter();
  }
  window.addEventListener('resize', () => {
    fatFooterInit();
  });
  fontBtn.forEach((i) => {
    i.addEventListener('click', function () {
      fatFooterInit();
      el.innerHTML = '展開/OPEN';
      el.setAttribute('name', '展開選單/OPEN');
      el.classList.remove('close');
    });
  });
}
fatFooter(); // fatFooter是否要展開
```

<!-- tabs:end -->

<!-- <iframe height="400" style="width: 100%;" scrolling="no" title="Fat-footer / 頁尾選單" src="https://codepen.io/u00hyui/embed/dyNxVWr?height=265&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/u00hyui/pen/dyNxVWr'>Fat-footer / 頁尾選單</a> by u00hyui
  (<a href='https://codepen.io/u00hyui'>@u00hyui</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe> -->

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<style>
    .markdown-section ul{
        padding: 0;
    }
    .fatFooter ul li ul li a{
        font-weight:400;
        color:#000;
    }
</style>
<script>
    function fatFooter(obj) {
  const el = document.querySelector('.btnFatFooter') || null; // --- 控制的對象
  const fontBtn = document.querySelectorAll('.fontSize ul li a');
  function fatFooterInit() {
    // --- 抓取UI高度 css樣式修改樣式重新抓取高度
    const _navUl = el.parentNode.querySelectorAll('nav ul li ul');
    setTimeout(() => {
      _navUl.forEach((i) => {
        i.setAttribute('style', '');
        let _itemHeight = i.offsetHeight;
        i.dataset.itemHeight = _itemHeight;
        if (Number(_itemHeight) !== 0) {
          i.style.height = `${Number(i.dataset.itemHeight)}px`;
        } else {
          i.style.height = '0px';
        }
      });
    }, 20);
  }
  function toggleFatFooter() {
    const _navUl = el.parentNode.querySelectorAll('nav ul li ul');
    _navUl.forEach((i) => {
      if (i.offsetHeight !== 0) {
        i.style.height = '0px';
        el.innerHTML = '收合/CLOSE';
        el.setAttribute('name', '收合選單/CLOSE');
      } else {
        i.style.height = `${i.dataset.itemHeight}px`;
        el.innerHTML = '展開/OPEN';
        el.setAttribute('name', '展開選單/OPEN');
      }
    });
    el.classList.toggle('close');
  }
  fatFooterInit();
  // --- 點擊時
  el.addEventListener('click', toggleFatFooterEle);
  function toggleFatFooterEle() {
    setTimeout(() => {
      el.addEventListener('click', toggleFatFooterEle);
    }, 500);
    el.removeEventListener('click', toggleFatFooterEle);
    toggleFatFooter();
  }
  window.addEventListener('resize', () => {
    fatFooterInit();
  });
  fontBtn.forEach((i) => {
    i.addEventListener('click', function () {
      fatFooterInit();
      el.innerHTML = '展開/OPEN';
      el.setAttribute('name', '展開選單/OPEN');
      el.classList.remove('close');
    });
  });
}
fatFooter(); // fatFooter是否要展開
</script>
