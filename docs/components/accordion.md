# Accordion 收合式選單

?>檔案名稱：sass/ module /`accordion.scss`

## 預設收合式選單樣式

點擊 `accordionList`，透過改變 `Class` 來顯示及隱藏另一個元素：

- `.accordionContent`會在轉換的過程中被套用。
- 透過 `.active` 來顯示內容。
- 透過 `.active` 來更改`.accordionBtn`顯示說明的文字。
<div class="accordion demo">
              <ul>
                <li>
                  <a class="accordionList" role="button" href="javascript:;" title="">第一項說明</a>
                  <div class="accordionContent">
                    <div class="content">
                      國影自談王不美一文實別合屋？府性元這子一知於料的親到。一用技年不得就資公，也星樣團怎英班水灣個種決以因世書發定很功行何，下飯通反代命假到一不離護麼錯絕懷旅元人。弟新過，道給仍覺裡水國、醫灣了可實界一上德字什心成但創大品隨品。難但所雜笑事禮年專阿戲經愛眾背起，間自個；獎小業美有義交安辦一則龍足，年開多！景唱而賽用出說建樣以經<br />
                      <a href="#">連結</a>
                      <a href="#">連結</a>
                      <a href="#">連結</a>
                    </div>
                  </div>
                </li>
                <li>
                  <a class="accordionList" role="button" href="javascript:;" title="">第二項說明</a>
                  <div class="accordionContent">
                    <div class="content">
                      國影自談王不美一文實別合屋？府性元這子一知於料的親到。一用技年不得就資公，也星樣團怎英班水灣個種決以因世書發定很功行何，下飯通反代命假到一不離護麼錯絕懷旅元人。弟新過，道給仍覺裡水國、醫灣了可實界一上德字什心成但創大品隨品。<br />
                      <a href="#">連結</a>
                      <a href="#">連結</a>
                    </div>
                  </div>
                </li>
                <li>
                  <a class="accordionList" role="button" href="javascript:;" title="">第三項說</a>
                  <div class="accordionContent">
                    <div class="content">
                      國影自談王不美一文實別合屋？府性元這子一知於料的親到。一用技年不得就資公，也星樣團怎英班水灣個種決以因世書發定很功行何，下飯通反代命假到一不離護麼錯絕懷旅元人。弟新過，道給仍覺裡水國、醫灣了可實界一上德字什心成但創大品隨品。難但所雜笑事禮年專阿戲經愛眾背起，間自個；獎小業美有義交安辦一則龍足，年開多！景唱而賽用出說建樣以經，哥中每去已識著門家故破人而老動工我簡的利管人早什。葉禮名交，都說為一失到就招投高畫。月錢產，機力燈自體日關工車之土庭，件年真經書？<br />
                      <a href="#">連結</a>
                    </div>
                  </div>
                </li>
              </ul>
            </div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="accordion">
  <ul>
    <li>
      <a class="accordionList" role="button" href="javascript:;" title="">第一項說明</a>
      <div class="accordionContent">
        <div class="content">
          .....<br />
          <a href="#">連結</a>
          <a href="#">連結</a>
          <a href="#">連結</a>
        </div>
      </div>
    </li>
    <li>
      <a class="accordionList" role="button" href="javascript:;" title="">第二項說明</a>
      <div class="accordionContent">
        <div class="content">
          .....<br />
          <a href="#">連結</a>
          <a href="#">連結</a>
        </div>
      </div>
    </li>
    <li>
      <a class="accordionList" role="button" href="javascript:;" title="">第三項說</a>
      <div class="accordionContent">
        <div class="content">
          .....<br />
          <a href="#">連結</a>
        </div>
      </div>
    </li>
  </ul>
</div>
```

#### **JavaScript**

```javascript
function accordionSlider(obj) {
  const accordionList = document.querySelectorAll(obj.accordionList);
  const accordion = document.querySelector(obj.accordionList) !== null ? document.querySelector(obj.accordionList).parentNode.parentNode : '';
  const accordionContent = obj.accordionContent;
  const accordionInfo = obj.accordionInfo.switch;
  const accordionInfoOpen = obj.accordionInfo.open;
  const accordionInfoClose = obj.accordionInfo.close;
  const fontBtn = document.querySelectorAll('.fontSize ul li a');
  // ---初始化
  fontBtn.forEach((i) => {
    i.addEventListener('click', function () {
      checkContentHeight();
    });
  });

  accordionList.forEach((i) => {
    i.innerHTML += `<span class="accordionBtn">${accordionInfoOpen}</span>`;
    i.innerHTML += `<span class="accordionArrow"></span>`;
  });

  // ---抓取高度
  function checkContentHeight() {
    accordionList.forEach((i) => {
      let itemContent = i.nextElementSibling;
      itemContent.setAttribute('style', '');
      itemContent.dataset.itemHeight = itemContent.offsetHeight;
      itemContent.style.height = 0;
      accordion.querySelectorAll('.active').forEach((s) => s.classList.remove('active'));
    });
    toggleAccordion();
  }
  // ---操控開合
  function toggleAccordion() {
    accordionList.forEach((i, index) => {
      const isFirstAccordion = index === 0; // --- 如果是第一個頁籤
      const contentHeight = i.nextElementSibling.dataset.itemHeight || 0;

      const thisPrevItem = accordionList[index - 1]; // --- 綁定前一個頁籤按鈕
      let prevItemAllA;
      if (thisPrevItem !== undefined) {
        prevItemAllA = thisPrevItem.nextElementSibling.querySelectorAll('[href], input'); // --- 前一個頁籤內容所有a和input項目
      }
      let prevItemLastA;
      if (thisPrevItem !== undefined) {
        prevItemLastA = prevItemAllA[prevItemAllA.length];
      }

      i.querySelector('.accordionBtn').innerHTML = `${accordionInfoOpen}`;
      i.addEventListener('keydown', (e) => {
        if (e.which === 9 && !e.shiftKey) {
          accordionList.forEach((s) => {
            s.nextElementSibling.style.height = `0px`;
            s.parentNode.classList.remove('active');
            s.querySelector('.accordionBtn').innerHTML = `${accordionInfoOpen}`;
          });
          i.nextElementSibling.style.height = `${contentHeight}px`;
          i.parentNode.classList.add('active');
          i.querySelector('.accordionBtn').innerHTML = `${accordionInfoClose}`;
        } else if (e.which === 9 && e.shiftKey && !isFirstAccordion) {
          if (prevItemAllA.length) {
            accordionList.forEach((s) => {
              s.nextElementSibling.style.height = `0px`;
              s.parentNode.classList.remove('active');
              s.querySelector('.accordionBtn').innerHTML = `${accordionInfoOpen}`;
            });
            accordionList[index - 1].parentNode.classList.add('active');
            accordionList[index - 1].nextElementSibling.style.height = `${accordionList[index - 1].nextElementSibling.dataset.itemHeight}px`;
            accordionList[index - 1].querySelector('.accordionBtn').innerHTML = `${accordionInfoClose}`;
          }
        }
      });

      i.addEventListener('click', (e) => {
        //取消Ａ連結預設行為
        e.preventDefault();
        accordionList.forEach((s) => {
          s.parentNode.classList.remove('active');
          s.nextElementSibling.style.height = `0px`;
          s.querySelector('.accordionBtn').innerHTML = `${accordionInfoOpen}`;
        });
        i.nextElementSibling.style.height = `${contentHeight}px`;
        i.parentNode.classList.add('active');
        i.querySelector('.accordionBtn').innerHTML = `${accordionInfoClose}`;
      });
    });
  }

  window.addEventListener('resize', (e) => {
    // --- 算出 menu 距離上方的高度
    setTimeout(() => {
      checkContentHeight();
      accordionList.forEach((v) => {
        v.parentNode.classList.remove('active');
        v.nextElementSibling.style.height = `0px`;
        v.querySelector('.accordionBtn').innerHTML = `${accordionInfoOpen}`;
      });
    }, 50);
  });
}
```

<!-- tabs:end -->

```javascript
// 手風琴功能
accordionSlider({
  list: '.accordionList', // 問題區塊
  content: '.accordionContent', // 回答區塊
  autoSlider: true,
  info: {
    open: '展開', // 收合時顯示
    close: '收合', // 展開時顯示
  },
});
```

## 用法

| Name       | Type                 | Default                     | Description                            |
| :--------- | :------------------- | --------------------------- | -------------------------------------- |
| list       | selector DOM element | .accordionList              | 問題區塊                               |
| content    | selector DOM element | .accordionContent           | 回答區塊                               |
| autoSlider | true / false         | true                        | 點選其他項目時是否要自動關閉已開啟項目 |
| info       | string               | open:'展開'｜ close: '收合' | 收合時顯示 / 展開時顯示                |

## 方法

| Method | Description          |
| :----- | :------------------- |
| open   | 展開時顯示的說明文字 |
| close  | 收合時顯示的說明文字 |

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<style>
.demo{
  margin:4em 0 ;
}  
  .accordion ul {
	list-style: none;
	padding: 0;
}
.accordion ul li {
	margin-bottom: 0.5em;
}
.accordion ul li .accordionList {
	display: block;
	background-color: #21baff;
	color: #fff;
	text-decoration: none;
	padding: 5px;
	position: relative;
}
.accordion .accordionContent {
	line-height: 1.45em;
	transition: height 0.3s linear;
	overflow: hidden;
}
.accordion .accordionContent .content {
	padding: 10px;
  position: relative;
    right: auto;
    left: auto;
}
.accordion .accordionBtn {
	margin-left: 10px;
}
.accordion .accordionArrow {
	position: absolute;
	right: 40px;
}
.accordion .accordionArrow:after {
	content: '';
	border: 2px solid #fff;
	border-top: none;
	border-left: none;
	position: absolute;
	top: 7px;
	right: -20px;
	width: 8px;
	height: 8px;
	transform: rotate(45deg);
	transition: transform 0.5s;
}
.accordion .accordionArrow.open:after {
	top: 8px;
	transform: rotate(225deg);
}
</style>
<script>
  function accordionSlider(obj) {
  const accordionList = document.querySelectorAll(obj.accordionList);
  const accordion = document.querySelector(obj.accordionList) !== null ? document.querySelector(obj.accordionList).parentNode.parentNode : '';
  const accordionContent = obj.accordionContent;
  const accordionInfo = obj.accordionInfo.switch;
  const accordionInfoOpen = obj.accordionInfo.open;
  const accordionInfoClose = obj.accordionInfo.close;
  accordionList.forEach((i) => {
    i.innerHTML += `<span class="accordionBtn">${accordionInfoOpen}</span>`;
    i.innerHTML += `<span class="accordionArrow"></span>`;
  });
  // ---抓取高度
  checkContentHeight();
  function checkContentHeight() {
    accordionList.forEach((i) => {
      let itemContent = i.nextElementSibling;
      itemContent.setAttribute('style', '');
      itemContent.dataset.itemHeight = itemContent.offsetHeight;
      itemContent.style.height = 0;
      accordion.querySelectorAll('.active').forEach((s) => s.classList.remove('active'));
    });
    toggleAccordion();
  }
  // ---操控開合
  function toggleAccordion() {
     console.log("3")
    accordionList.forEach((i, index) => {
      const isFirstAccordion = index === 0; // --- 如果是第一個頁籤
      const contentHeight = i.nextElementSibling.dataset.itemHeight || 0;
      const thisPrevItem = accordionList[index - 1]; // --- 綁定前一個頁籤按鈕
      let prevItemAllA;
      if (thisPrevItem !== undefined) {
        prevItemAllA = thisPrevItem.nextElementSibling.querySelectorAll('[href], input'); // --- 前一個頁籤內容所有a和input項目
      }
      let prevItemLastA;
      if (thisPrevItem !== undefined) {
        prevItemLastA = prevItemAllA[prevItemAllA.length];
      }
      i.querySelector('.accordionBtn').innerHTML = `${accordionInfoOpen}`;
      i.addEventListener('keydown', (e) => {
        if (e.which === 9 && !e.shiftKey) {
          accordionList.forEach((s) => {
            s.nextElementSibling.style.height = `0px`;
            s.parentNode.classList.remove('active');
            s.querySelector('.accordionBtn').innerHTML = `${accordionInfoOpen}`;
          });
          i.nextElementSibling.style.height = `${contentHeight}px`;
          i.parentNode.classList.add('active');
          i.querySelector('.accordionBtn').innerHTML = `${accordionInfoClose}`;
        } else if (e.which === 9 && e.shiftKey && !isFirstAccordion) {
          if (prevItemAllA.length) {
            accordionList.forEach((s) => {
              s.nextElementSibling.style.height = `0px`;
              s.parentNode.classList.remove('active');
              s.querySelector('.accordionBtn').innerHTML = `${accordionInfoOpen}`;
            });
            accordionList[index - 1].parentNode.classList.add('active');
            accordionList[index - 1].nextElementSibling.style.height = `${accordionList[index - 1].nextElementSibling.dataset.itemHeight}px`;
            accordionList[index - 1].querySelector('.accordionBtn').innerHTML = `${accordionInfoClose}`;
          }
        }
      });
      i.addEventListener('click', (e) => {
        //取消Ａ連結預設行為
        e.preventDefault();
        accordionList.forEach((s) => {
          s.parentNode.classList.remove('active');
          s.nextElementSibling.style.height = `0px`;
          s.querySelector('.accordionBtn').innerHTML = `${accordionInfoOpen}`;
        });
        i.nextElementSibling.style.height = `${contentHeight}px`;
        i.parentNode.classList.add('active');
        i.querySelector('.accordionBtn').innerHTML = `${accordionInfoClose}`;
      });
    });
  }
  window.addEventListener('resize', (e) => {
    // --- 算出 menu 距離上方的高度
    setTimeout(() => {
      checkContentHeight();
      accordionList.forEach((v) => {
        v.parentNode.classList.remove('active');
        v.nextElementSibling.style.height = `0px`;
        v.querySelector('.accordionBtn').innerHTML = `${accordionInfoOpen}`;
      });
    }, 50);
  });
}
// 手風琴功能
accordionSlider({
  accordionList: '.accordionList', // 問題區塊
  accordionContent: '.accordionContent', // 回答區塊
  accordionInfo: {
    open: '展開', // 收合時顯示
    close: '收合', // 展開時顯示
  },
});
</script>
