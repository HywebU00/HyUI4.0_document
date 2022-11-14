# Function Panel / 內容頁控制及顯示模組

?>檔案名稱：sass/ module / `_function_panel.scss`

> 可自由組合 `發布日期`、`文字大小`、`回上一頁`、`友善列印`、`轉寄友人`、`社群分享`...等目前以提供之模組，在父層包覆 1 個 `functionPanel` 的 div，即可呈現以下樣式。 ，模組無需更改結構只需要放進 `functionPanel` 的 div 即可。

預設包含：

- 發布時間
- 文字大小
- 回上一頁
- 友善列印
- 轉寄友人
- 社群分享

<!-- functionPanel -->
   <div class="functionPanel">
              <div class="publishTime"><span>發布日期：</span><time>2019-01-01</time></div>
              <!-- 文字大小 -->
              <div class="fontSize">
                <span>字型大小：</span>
                <!-- 英文用<span>font-size：</span> -->
                <ul>
                  <li><a role="button" href="#" class="small">小</a></li>
                  <li><a role="button" href="#" class="medium">中</a></li>
                  <li><a role="button" href="#" class="large">大</a></li>
                </ul>
              </div>
              <!-- function功能區塊 -->
              <div class="function">
                <ul>
                  <li class="back"><a href="javascript:history.back()">回上一頁</a></li>
                  <li class="print"><a href="#">友善列印</a></li>
                  <li class="forward"><a href="#">轉寄友人</a></li>
                </ul>
              </div>
              <!-- 社群分享 -->
              <div class="share">
                <ul>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_facebook.svg" alt="facebook" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_twitter.svg" alt="twitter" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_line.svg" alt="line" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_youtube.svg" alt="youtube" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_googleplus.svg" alt="google plus" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_instagram.svg" alt="instagram" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_linkedin.svg" alt="LinkedIn" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_rss.svg" alt="RSS" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_plurk.svg" alt="Plurk" /></a>
      </li>
    </ul>
              </div>
            </div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="functionPanel">
  <div class="publishTime"><span>發布日期：</span><time>2019-01-01</time></div>
  <!-- 文字大小 -->
  <div class="fontSize">
    <span>字型大小：</span>
    <!-- 英文用<span>font-size：</span> -->
    <ul>
      <li><a role="button" href="#" class="small">小</a></li>
      <li><a role="button" href="#" class="medium">中</a></li>
      <li><a role="button" href="#" class="large">大</a></li>
    </ul>
  </div>
  <!-- function功能區塊 -->
  <div class="function">
    <ul>
      <li class="back"><a href="javascript:history.back()">回上一頁</a></li>
      <li class="print"><a href="#">友善列印</a></li>
      <li class="forward"><a href="#">轉寄友人</a></li>
    </ul>
  </div>
  <!-- 社群分享 -->
  <div class="share">
    <ul>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_facebook.svg" alt="facebook" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_twitter.svg" alt="twitter" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_line.svg" alt="line" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_youtube.svg" alt="youtube" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_googleplus.svg" alt="google plus" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_instagram.svg" alt="instagram" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_linkedin.svg" alt="LinkedIn" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_rss.svg" alt="RSS" /></a>
      </li>
      <li>
        <a href="#"><img src="https://hywebu00.github.io/HyUI_v4.0/images/basic/icon_plurk.svg" alt="Plurk" /></a>
      </li>
    </ul>
  </div>
</div>
```

<!-- tabs:end -->
<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<style>
  .functionPanel .share ul{
    padding-left: 0.5rem;
  }
  .functionPanel .publishTime:before {
    margin-right: 0.5em;
  }
  .fontSize a{
    color: #000 !important;
    font-weight: 400 !important;
  }
  .fontSize a:hover{
    color:#fff !important;
  }
</style>
<script>
const slider = (function () {
  let Slider = {};
  function TimerManager() {
    this.timers = [];
    this.args = [];
    this.isTimerRun = false;
  }
  TimerManager.makeTimerManage = function (element) {
    if (!element.TimerManage || element.TimerManage.constructor !== TimerManager) {
      element.TimerManage = new TimerManager();
    }
  };
  TimerManager.prototype.add = function (timer, args) {
    this.timers.push(timer);
    this.args.push(args);
    this.timerRun();
  };
  TimerManager.prototype.timerRun = function () {
    if (!this.isTimerRun) {
      let timer = this.timers.shift(),
        args = this.args.shift();
      if (timer && args) {
        this.isTimerRun = true;
        timer(args[0], args[1]);
      }
    }
  };
  TimerManager.prototype.next = function () {
    this.isTimerRun = false;
    this.timerRun();
  };
  function jsSlideUp(element, time) {
    if (element.offsetHeight > 0) {
      let totalHeight = element.offsetHeight;
      let currentHeight = totalHeight;
      let reduceValue = totalHeight / (time / 10);
      element.style.transition = 'height ' + time + ' ms';
      element.style.overflow = 'hidden';
      let timer = setInterval(function () {
        currentHeight -= reduceValue;
        element.style.height = currentHeight + 'px';
        if (currentHeight <= 0) {
          clearInterval(timer);
          element.style.display = 'none';
          element.style.height = totalHeight + 'px';
          if (element.TimerManage && element.TimerManage.constructor === TimerManager) {
            element.TimerManage.next();
          }
        }
      }, 10);
    } else {
      if (element.TimerManage && element.TimerManage.constructor === TimerManager) {
        element.TimerManage.next();
      }
    }
  }
  function jsSlideDown(element, time) {
    if (element.offsetHeight <= 0) {
      element.style.display = 'block';
      element.style.transition = 'height' + time + ' ms';
      element.style.overflow = 'hidden';
      let totalHeight = element.offsetHeight;
      let currentHeight = 0;
      element.style.height = '0px';
      let addValue = totalHeight / (time / 10);
      let timer = setInterval(function () {
        currentHeight += addValue;
        element.style.height = currentHeight + 'px';
        if (currentHeight >= totalHeight) {
          clearInterval(timer);
          element.style.height = totalHeight + 'px';
          if (element.TimerManage && element.TimerManage.constructor === TimerManager) {
            element.TimerManage.next();
          }
        }
      }, 10);
    } else {
      if (element.TimerManage && element.TimerManage.constructor === TimerManager) {
        element.TimerManage.next();
      }
    }
  }
  // the interface about slideUp method
  Slider.jsSlideUp = function (element) {
    TimerManager.makeTimerManage(element);
    element.TimerManage.add(jsSlideUp, arguments);
    return this;
  };
  // the interface about slideDown method
  Slider.jsSlideDown = function (element) {
    TimerManager.makeTimerManage(element);
    element.TimerManage.add(jsSlideDown, arguments);
    return this;
  };
  return Slider;
})();
  class SelectSlider {
  constructor(obj) {
    this.name = obj.name || null; // --- 按鈕列表名稱
    this.control = obj.control || null; // --- 控制的對象名稱
  }
  // --- 點擊 語言模組
  sliderClick() {
    this.name.forEach((i) => {
      i.addEventListener('click', (e) => {
        e.preventDefault();
        const sliderItem = e.target.nextElementSibling;
        if (sliderItem === null) {
          return;
        } else if (sliderItem.offsetHeight !== 0 || sliderItem.offsetHeight === null) {
          slider.jsSlideUp(sliderItem, 300);
        } else {
          slider.jsSlideDown(sliderItem, 300);
        }
        this.sliderClose(e.target);
      });
    });
  }
  // --- Keydown 語言模組
  sliderKeydown() {
    this.control.forEach((i) => {
      i.addEventListener('keydown', (e) => {
        const sliderItem = e.target.nextElementSibling;
        if (sliderItem) {
          slider.jsSlideDown(sliderItem, 300);
        }
      });
    });
  }
  // --- Focusout 語言模組
  sliderFocusout() {
    this.name.forEach((i) => {
      const nodes = i.querySelectorAll('ul li a');
      const lastNodes = nodes[nodes.length - 1];
      const sliderItem = i.querySelector('ul');
      lastNodes.addEventListener('focusout', (e) => {
        e.preventDefault();
        slider.jsSlideUp(sliderItem, 300);
      });
    });
  }
  // --- 關閉語言模組
  sliderClose(item) {
    const sliderItem = item.nextElementSibling;
    const that = this;
    function clickOtherPlace(e) {
      const chooseClassName = that.name[0].className;
      if (e.target.closest(`.${chooseClassName}`) === null) {
        slider.jsSlideUp(sliderItem, 300);
      } else {
        return;
      }
    }
    document.addEventListener('touchstart', (e) => {
      e.preventDefault();
      clickOtherPlace(e);
    });
    document.addEventListener('click', clickOtherPlace);
  }
  initial() {
    this.sliderClick();
    this.sliderKeydown();
    this.sliderFocusout();
  }
}
  function shareBtnFunction() {
  // --- 創造一個a連結的按鈕
  const shareUl = document.querySelector('.share');
  const btn = document.createElement('a');
  if (shareUl) {
    btn.setAttribute('class', 'shareButton');
    btn.setAttribute('role', 'button');
    btn.textContent = 'share分享按鈕';
    shareUl.insertBefore(btn, shareUl.childNodes[0]);
  }
  const shareBtn = new SelectSlider({
    name: document.querySelectorAll('.share'), // --- 控制的對象
    control: document.querySelectorAll('.share a'), // --- 監聽的對象
  });
  shareBtn.initial();
}
shareBtnFunction();
</script>
<!-- <iframe height="400" style="width: 100%;" scrolling="no" title="Function Panel / 內容頁控制及顯示模組" src="https://codepen.io/u00hyui/embed/qBrWbRr?defaultTab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/qBrWbRr">
  Function Panel / 內容頁控制及顯示模組</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe> -->
