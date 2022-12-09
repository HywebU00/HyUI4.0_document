# Accordion 收合式選單

?>檔案名稱：sass/ module /`accordion.scss`

## 預設收合式選單樣式

點擊 `accordionList`，透過改變 `Class` 來顯示及隱藏另一個元素：

- `.accordionContent`會在轉換的過程中被套用。
- 透過 `.active` 來顯示內容。
- 透過 `.active` 來更改`.accordionBtn`顯示說明的文字。

<div class="accordion">
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
      <a class="accordionList" role="button" href="javascript:;" title="">第三項說明</a>
      <div class="accordionContent">
        <div class="content">
          國影自談王不美一文實別合屋？府性元這子一知於料的親到。一用技年不得就資公，也星樣團怎英班水灣個種決以因世書發定很功行何，下飯通反代命假到一不離護麼錯絕懷旅元人。弟新過，道給仍覺裡水國、醫灣了可實界一上德字什心成但創大品隨品。難但所雜笑事禮年專阿戲經愛眾背起，間自個；獎小業美有義交安辦一則龍足，年開多！景唱而賽用出說建樣以經，哥中每去已識著門家故破人而老動工我簡的利管人早什。葉禮名交，都說為一失到就招投高畫。月錢產，機力燈自體日關工車之土庭，件年真經書？<br />
          <a href="#">連結</a>
        </div>
      </div>
    </li>
    <li>
      <a class="accordionList" role="button" href="javascript:;" title="">第四項說明</a>
      <div class="accordionContent">
        <div class="content">
          國影自談王不美一文實別合屋？府性元這子一知於料的親到。一用技年不得就資公，也星樣團怎英班水灣個種決以因世書發定很功行何，下飯通反代命假到一不離護麼錯絕懷旅元人。弟新過，道給仍覺裡水國、醫灣了可實界一上德字什心成但創大品隨品。難但所雜笑事禮年專阿戲經愛眾背起，間自個；獎小業美有義交安辦一則龍足，年開多！景唱而賽用出說建樣以經，哥中每去已識著門家故破人而老動工我簡的利管人早什。葉禮名交，都說為一失到就招投高畫。月錢產，機力燈自體日關工車之土庭，件年真經書？<br />
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
          ...<br />
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
          ...<br />
          <a href="#">連結</a>
          <a href="#">連結</a>
        </div>
      </div>
    </li>
    <li>
      <a class="accordionList" role="button" href="javascript:;" title="">第三項說明</a>
      <div class="accordionContent">
        <div class="content">
          ...<br />
          <a href="#">連結</a>
        </div>
      </div>
    </li>
    <li>
      <a class="accordionList" role="button" href="javascript:;" title="">第四項說明</a>
      <div class="accordionContent">
        <div class="content">...<br /></div>
      </div>
    </li>
  </ul>
</div>
```

#### **JavaScript**

```javascript
function accordionSlider(obj) {
  const list = document.querySelectorAll(obj.list);
  let { autoSlider } = obj;
  const { open, close } = obj.info;
  const duration = obj.duration || 300;
  list.forEach((item, index) => {
    let random = randomLetter(4) + randomFloor(0, 9999);
    let contentA = item.nextElementSibling.querySelectorAll('[href],input,button');
    let content = item.parentElement.querySelector('.accordionContent');
    let contentFirstA = contentA[0];
    item.innerHTML += `<span class="accordionBtn">${open}</span>`;
    item.innerHTML += `<span class="accordionArrow"></span>`;
    item.setAttribute('aria-expanded', 'false');
    item.setAttribute('aria-controls', random);
    content.setAttribute('id', random);
    item.addEventListener('click', function () {
      toggleAccordion(item, index, content);
    });
    //無障礙
    item.addEventListener('keydown', (e) => {
      if (e.which === 9 && !e.shiftKey) {
        if (!item.parentElement.classList.contains('active')) {
          toggleAccordion(item, index, content);
        }
      } else if (e.which === 9 && e.shiftKey) {
        if (autoSlider) {
          e.preventDefault();
          toggleAccordion(item, index, content);
          if (contentA.length) {
            contentA[contentA.length - 1].focus();
          } else {
            list[index - 1].focus();
          }
        } else {
          toggleAccordion(item, index, content);
        }
      }
    });
    if (contentFirstA !== undefined && autoSlider) {
      contentFirstA.addEventListener('keydown', (e) => {
        if (e.which === 9 && e.shiftKey) {
          list[index].focus();
        }
      });
    }
  });
  //亂數產生數字
  function randomFloor(min, max) {
    return Math.floor(Math.random() * (max - min + 1) + min);
  }
  // 亂數產生英文字
  function randomLetter(max) {
    var text = '';
    var letter = 'abcdefghijklmnopqrstuvwxyz';

    for (let i = 0; i < max; i++) text += letter.charAt(Math.floor(Math.random() * letter.length));
    return text;
  }

  function toggleAccordion(item, index, content) {
    let display = window.getComputedStyle(content).display;
    item.parentElement.classList.add('active');
    content.style.display = display;

    if (display === 'none') {
      display = 'block';
      content.style.display = display;
      content.style.overflow = 'hidden';
      item.setAttribute('aria-expanded', 'true');
      let height = content.offsetHeight;
      content.style.height = 0;
      content.offsetHeight;
      content.style.transitionProperty = 'height';
      content.style.transitionDuration = `${duration}ms`;
      content.style.height = height + 'px';
      item.querySelector('.accordionBtn').innerHTML = `${close}`;
      if (autoSlider) {
        const siblings = [...item.parentNode.parentNode.children].filter((child) => {
          return child !== item.parentNode;
        });
        siblings.forEach((v) => {
          v.classList.remove('active');
          item.setAttribute('aria-expanded', 'false');
          let siblingsContent = v.querySelector('.accordionContent');
          siblingsContent.style.overflow = 'hidden';
          siblingsContent.style.height = `${siblingsContent.offsetHeight}px`;
          siblingsContent.style.transitionProperty = 'height';
          siblingsContent.style.transitionDuration = `${duration}ms`;
          siblingsContent.offsetHeight;
          siblingsContent.style.height = 0;
          v.querySelector('.accordionBtn').innerHTML = `${open}`;
          window.setTimeout(() => {
            siblingsContent.style.display = 'none';
            siblingsContent.style.removeProperty('overflow');
            siblingsContent.style.removeProperty('height');
            siblingsContent.style.removeProperty('transition-duration');
            siblingsContent.style.removeProperty('transition-property');
          }, duration);
        });
      }
      setTimeout(() => {
        content.style.removeProperty('overflow');
        content.style.removeProperty('height');
        content.style.removeProperty('transition-duration');
        content.style.removeProperty('transition-property');
      }, duration);
    } else {
      item.setAttribute('aria-expanded', 'false');
      content.style.overflow = 'hidden';
      content.style.height = `${content.offsetHeight}px`;
      content.style.transitionProperty = 'height';
      content.style.transitionDuration = `${duration}ms`;
      content.offsetHeight;
      content.style.height = 0;
      item.querySelector('.accordionBtn').innerHTML = `${open}`;
      item.parentElement.classList.remove('active');
      setTimeout(() => {
        content.style.display = 'none';
        content.style.removeProperty('overflow');
        content.style.removeProperty('height');
        content.style.removeProperty('transition-duration');
        content.style.removeProperty('transition-property');
      }, duration);
    }
  }
}
```

```javascript
// 手風琴功能
accordionSlider({
  list: '.accordionList', // 問題區塊
  content: '.accordionContent', // 回答區塊
  autoSlider: true, // true 點選其他項目時會關閉已開啟的內容，false 需要再點一次才會關閉
  duration: 300, // 展開/縮起時間
  info: {
    open: '展開', // 收合時顯示
    close: '收合', // 展開時顯示
  },
});
```

<!-- tabs:end -->

## 用法

| Name       | Type                 | Default                     | Description                            |
| :--------- | :------------------- | --------------------------- | -------------------------------------- |
| list       | selector DOM element | .accordionList              | 問題區塊                               |
| content    | selector DOM element | .accordionContent           | 回答區塊                               |
| autoSlider | true / false         | true                        | 點選其他項目時是否要自動關閉已開啟項目 |
| duration   | number               | 300                         | 展開/縮起時間                          |
| info       | string               | open:'展開'｜ close: '收合' | 收合時顯示 / 展開時顯示                |

## 方法

| Method | Description          |
| :----- | :------------------- |
| open   | 展開時顯示的說明文字 |
| close  | 收合時顯示的說明文字 |

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<style>
.demo {
  margin: 4em 0;
}
.accordion ul{
  padding:0px
}
.accordion .accordionList{
  color:#FFF;
}
.accordion .content{
  position:relative;
  padding-top:0px;
  left:auto;
}
</style>
<script>
function accordionSlider(obj) {
  const list = document.querySelectorAll(obj.list);
  let { autoSlider } = obj;
  const { open, close } = obj.info;
  const duration = obj.duration || 300;
  list.forEach((item, index) => {
    let random = randomLetter(4) + randomFloor(0, 9999);
    let contentA = item.nextElementSibling.querySelectorAll('[href],input,button');
    let content = item.parentElement.querySelector('.accordionContent');
    let contentFirstA = contentA[0];
    item.innerHTML += `<span class="accordionBtn">${open}</span>`;
    item.innerHTML += `<span class="accordionArrow"></span>`;
    item.setAttribute('aria-expanded', 'false');
    item.setAttribute('aria-controls', random);
    content.setAttribute('id', random);
    item.addEventListener('click', function () {
      toggleAccordion(item, index, content);
    });
    //無障礙
    item.addEventListener('keydown', (e) => {
      if (e.which === 9 && !e.shiftKey) {
        if (!item.parentElement.classList.contains('active')) {
          toggleAccordion(item, index, content);
        }
      } else if (e.which === 9 && e.shiftKey) {
        if (autoSlider) {
          e.preventDefault();
          toggleAccordion(item, index, content);
          if (contentA.length) {
            contentA[contentA.length - 1].focus();
          } else {
            list[index - 1].focus();
          }
        } else {
          toggleAccordion(item, index, content);
        }
      }
    });
    if (contentFirstA !== undefined && autoSlider) {
      contentFirstA.addEventListener('keydown', (e) => {
        if (e.which === 9 && e.shiftKey) {
          list[index].focus();
        }
      });
    }
  });
  //亂數產生數字
  function randomFloor(min, max) {
    return Math.floor(Math.random() * (max - min + 1) + min);
  }
  // 亂數產生英文字
  function randomLetter(max) {
    var text = '';
    var letter = 'abcdefghijklmnopqrstuvwxyz';
    for (let i = 0; i < max; i++) text += letter.charAt(Math.floor(Math.random() * letter.length));
    return text;
  }
  function toggleAccordion(item, index, content) {
    let display = window.getComputedStyle(content).display;
    item.parentElement.classList.add('active');
    content.style.display = display;
    if (display === 'none') {
      display = 'block';
      content.style.display = display;
      content.style.overflow = 'hidden';
      item.setAttribute('aria-expanded', 'true');
      let height = content.offsetHeight;
      content.style.height = 0;
      content.offsetHeight;
      content.style.transitionProperty = 'height';
      content.style.transitionDuration = `${duration}ms`;
      content.style.height = height + 'px';
      item.querySelector('.accordionBtn').innerHTML = `${close}`;
      if (autoSlider) {
        const siblings = [...item.parentNode.parentNode.children].filter((child) => {
          return child !== item.parentNode;
        });
        siblings.forEach((v) => {
          v.classList.remove('active');
          item.setAttribute('aria-expanded', 'false');
          let siblingsContent = v.querySelector('.accordionContent');
          siblingsContent.style.overflow = 'hidden';
          siblingsContent.style.height = `${siblingsContent.offsetHeight}px`;
          siblingsContent.style.transitionProperty = 'height';
          siblingsContent.style.transitionDuration = `${duration}ms`;
          siblingsContent.offsetHeight;
          siblingsContent.style.height = 0;
          v.querySelector('.accordionBtn').innerHTML = `${open}`;
          window.setTimeout(() => {
            siblingsContent.style.display = 'none';
            siblingsContent.style.removeProperty('overflow');
            siblingsContent.style.removeProperty('height');
            siblingsContent.style.removeProperty('transition-duration');
            siblingsContent.style.removeProperty('transition-property');
          }, duration);
        });
      }
      setTimeout(() => {
        content.style.removeProperty('overflow');
        content.style.removeProperty('height');
        content.style.removeProperty('transition-duration');
        content.style.removeProperty('transition-property');
      }, duration);
    } else {
      item.setAttribute('aria-expanded', 'false');
      content.style.overflow = 'hidden';
      content.style.height = `${content.offsetHeight}px`;
      content.style.transitionProperty = 'height';
      content.style.transitionDuration = `${duration}ms`;
      content.offsetHeight;
      content.style.height = 0;
      item.querySelector('.accordionBtn').innerHTML = `${open}`;
      item.parentElement.classList.remove('active');
      setTimeout(() => {
        content.style.display = 'none';
        content.style.removeProperty('overflow');
        content.style.removeProperty('height');
        content.style.removeProperty('transition-duration');
        content.style.removeProperty('transition-property');
      }, duration);
    }
  }
}
// 手風琴功能
accordionSlider({
  list: '.accordionList', // 問題區塊
  content: '.accordionContent', // 回答區塊
  autoSlider: true, // true 點選其他項目時會關閉已開啟的內容，false 需要再點一次才會關閉
  duration:300, // 展開/縮起時間
  info: {
    open: '展開', // 收合時顯示
    close: '收合', // 展開時顯示
  },
});
</script>
