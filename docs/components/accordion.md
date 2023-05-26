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
                  <button class="accordionList" role="button" title="">第一項說明</button>
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
                  <button class="accordionList" role="button" title="">第二項說明</button>
                  <div class="accordionContent">
                    <div class="content">
                      國影自談王不美一文實別合屋？府性元這子一知於料的親到。一用技年不得就資公，也星樣團怎英班水灣個種決以因世書發定很功行何，下飯通反代命假到一不離護麼錯絕懷旅元人。弟新過，道給仍覺裡水國、醫灣了可實界一上德字什心成但創大品隨品。<br />
                      <a href="#">連結</a>
                      <a href="#">連結</a>
                    </div>
                  </div>
                </li>
                <li>
                  <button class="accordionList" role="button" title="">第三項說明</button>
                  <div class="accordionContent">
                    <div class="content">
                      國影自談王不美一文實別合屋？府性元這子一知於料的親到。一用技年不得就資公，也星樣團怎英班水灣個種決以因世書發定很功行何，下飯通反代命假到一不離護麼錯絕懷旅元人。弟新過，道給仍覺裡水國、醫灣了可實界一上德字什心成但創大品隨品。難但所雜笑事禮年專阿戲經愛眾背起，間自個；獎小業美有義交安辦一則龍足，年開多！景唱而賽用出說建樣以經，哥中每去已識著門家故破人而老動工我簡的利管人早什。葉禮名交，都說為一失到就招投高畫。月錢產，機力燈自體日關工車之土庭，件年真經書？<br />
                      <a href="#">連結</a>
                    </div>
                  </div>
                </li>
                <li>
                  <button class="accordionList" role="button" title="">第四項說明</button>
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
// 亂數數字
function randomFloor(min, max) {
  return Math.floor(Math.random() * (max - min + 1) + min);
}
// 亂數英文字
function randomLetter(max) {
  var text = '';
  var letter = 'abcdefghijklmnopqrstuvwxyz';
  for (let i = 0; i < max; i++) text += letter.charAt(Math.floor(Math.random() * letter.length));
  return text;
}
function accordionFunction(obj) {
  'use strict';
  const accordion = document.querySelector(obj.accordion);
  const accordionItem = accordion ? accordion.querySelectorAll('.accordionList') : '';
  const autoClose = obj.autoClose;
  const duration = obj.duration;
  const openFirst = obj.openFirst;
  const { open, close } = obj.info;

  function a11y() {
    if (Boolean(accordionItem)) {
      accordionItem.forEach((item, index) => {
        let content = item.nextElementSibling.querySelectorAll('a,input,select,textarea');
        let firstItem = false;

        if (!openFirst) {
          item.addEventListener('keydown', function (e) {
            if (e.which === 9 && !e.shiftKey) {
              autoClose && !openFirst ? closeOther(this) : '';
              openTarget(this);
              firstItem = false;
            } else if (e.which === 9 && e.shiftKey && !firstItem) {
              e.preventDefault();
              openTarget(this);
              autoClose && !openFirst ? closeOther(this) : '';

              if (content.length == 0) {
                accordionItem[index - 1].focus();
              } else if (content.length > 0) {
                content[content.length - 1].focus();
              }
            }
          });
          if (content.length !== 0) {
            content[0].addEventListener('keydown', function (e) {
              if (e.which === 9 && e.shiftKey && index !== 0) {
                e.preventDefault();
                accordionItem[index - 1].focus();
              } else if (e.which === 9 && e.shiftKey && index == 0) {
                firstItem = true;
                autoClose && !openFirst ? openTarget(accordionItem[0]) : '';
              }
            });
          }
        }
      });
    }
  }
  function info() {
    if (Boolean(accordionItem)) {
      accordionItem.forEach((item, index) => {
        let random = `accordion_${randomLetter(4)}${randomFloor(0, 9999)}`;
        item.innerHTML += `<span class="accordionState">${open}</span>`;
        item.innerHTML += `<span class="accordionArrow"></span>`;
        item.setAttribute('aria-expanded', 'false');
        item.setAttribute('aria-controls', random);
        item.parentElement.querySelector('.accordionContent').setAttribute('id', random);
        if (openFirst) {
          item.nextElementSibling.style.display = `block`;
        }
      });
    }
  }
  function clickFunction() {
    if (Boolean(accordionItem)) {
      accordionItem.forEach((item, index) => {
        item.addEventListener('click', function () {
          autoClose && !openFirst ? closeOther(this) : '';
          openTarget(this);
        });
      });
    }
  }

  function openTarget(item) {
    let content = item.nextElementSibling;
    let display = window.getComputedStyle(content).display;
    content.style.display = display;

    if (display === 'none') {
      display = 'block';
      item.parentNode.classList.add('active');
      item.setAttribute('aria-expanded', 'true');
      content.style.display = 'block';
      let contentHeight = content.scrollHeight;
      content.style.height = '0';
      content.style.transitionProperty = 'height';
      content.style.transitionDuration = `${duration}ms`;
      content.scrollHeight;
      item.querySelector('.accordionState').innerHTML = `${close}`;
      content.style.height = `${contentHeight}px`;
      setTimeout(() => {
        content.style.removeProperty('height');
        content.style.removeProperty('transition-duration');
        content.style.removeProperty('transition-property');
      }, duration);
    } else {
      let contentHeight = content.scrollHeight;
      content.style.height = `${contentHeight}px`;
      content.style.transitionProperty = 'height';
      content.style.transitionDuration = `${duration}ms`;
      content.scrollHeight;
      content.style.height = '0';
      item.querySelector('.accordionState').innerHTML = `${open}`;
      item.parentNode.classList.remove('active');
      item.setAttribute('aria-expanded', 'false');
      setTimeout(() => {
        content.style.removeProperty('height');
        content.style.removeProperty('display');
        content.style.removeProperty('transition-duration');
        content.style.removeProperty('transition-property');
      }, duration);
    }
  }
  function closeOther(item) {
    const siblings = [...item.parentNode.parentNode.children].filter((child) => {
      return child !== item.parentNode;
    });
    siblings.forEach((otherItem, index) => {
      let content = otherItem.querySelector('.accordionContent');
      if (content.style.Height !== 0 || content.style.Height !== null) {
        otherItem.querySelector('.accordionState').innerHTML = `${open}`;
        otherItem.classList.remove('active');
        otherItem.querySelector('.accordionList').setAttribute('aria-expanded', 'false');
        let contentHeight = content.scrollHeight;
        content.style.height = `${contentHeight}px`;
        content.style.transitionProperty = 'height';
        content.style.transitionDuration = `${duration}ms`;
        content.scrollHeight;
        content.style.height = '0';
        setTimeout(() => {
          content.style.removeProperty('height');
          content.style.removeProperty('display');
          content.style.removeProperty('transition-duration');
          content.style.removeProperty('transition-property');
        }, duration);
      }
    });
  }
  (function () {
    clickFunction();
    a11y();
    info();
  })();
}
```

```javascript
手風琴功能;
accordionFunction({
  accordion: '.accordion',
  openFirst: false, // 預設先展開所有內容，使用無障礙遊走不再有手風琴效果，永遠展開內容(滑鼠點擊正常開合)
  autoClose: true, // 若需要此功能需要關閉openFirst
  duration: 200,
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
| autoSlider | Boolean              | true                        | 點選其他項目時是否要自動關閉已開啟項目 |
| duration   | number               | 300                         | 展開/縮起時間                          |
| info       | string               | open:'展開'｜ close: '收合' | 收合時顯示 / 展開時顯示                |

## 方法

| Method | Description          |
| :----- | :------------------- |
| open   | 展開時顯示的說明文字 |
| close  | 收合時顯示的說明文字 |

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4/css/style.css" />
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
// 亂數數字
function randomFloor(min, max) {
  return Math.floor(Math.random() * (max - min + 1) + min);
}  
// 亂數英文字
function randomLetter(max) {
  var text = '';
  var letter = 'abcdefghijklmnopqrstuvwxyz';
  for (let i = 0; i < max; i++) text += letter.charAt(Math.floor(Math.random() * letter.length));
  return text;
};
function accordionFunction(obj) {
  const accordion = document.querySelector(obj.accordion);
  const accordionItem = accordion ? accordion.querySelectorAll('.accordionList') : '';
  const autoClose = obj.autoClose;
  const duration = obj.duration;
  const openFirst = obj.openFirst;
  const { open, close } = obj.info;
  function a11y() {
    if (Boolean(accordionItem)) {
      accordionItem.forEach((item, index) => {
        let content = item.nextElementSibling.querySelectorAll('a,input,select,textarea');
        let firstItem = false;
        if (!openFirst) {
          item.addEventListener('keydown', function (e) {
            if (e.which === 9 && !e.shiftKey) {
              autoClose && !openFirst ? closeOther(this) : '';
              openTarget(this);
              firstItem = false;
            } else if (e.which === 9 && e.shiftKey && !firstItem) {
              e.preventDefault();
              openTarget(this);
              autoClose && !openFirst ? closeOther(this) : '';
              if (content.length == 0) {
                accordionItem[index - 1].focus();
              } else if (content.length > 0) {
                content[content.length - 1].focus();
              }
            }
          });
          if (content.length !== 0) {
            content[0].addEventListener('keydown', function (e) {
              if (e.which === 9 && e.shiftKey && index !== 0) {
                e.preventDefault();
                accordionItem[index - 1].focus();
              } else if (e.which === 9 && e.shiftKey && index == 0) {
                firstItem = true;
                autoClose && !openFirst ? openTarget(accordionItem[0]) : '';
              }
            });
          }
        }
      });
    }
  }
  function info() {
    if (Boolean(accordionItem)) {
      accordionItem.forEach((item, index) => {
        let random = `accordion_${randomLetter(4)}${randomFloor(0, 9999)}`;
        item.innerHTML += `<span class="accordionState">${open}</span>`;
        item.innerHTML += `<span class="accordionArrow"></span>`;
        item.setAttribute('aria-expanded', 'false');
        item.setAttribute('aria-controls', random);
        item.parentElement.querySelector('.accordionContent').setAttribute('id', random);
        if (openFirst) {
          item.nextElementSibling.style.display = `block`;
        }
      });
    }
  }
  function clickFunction() {
    if (Boolean(accordionItem)) {
      accordionItem.forEach((item, index) => {
        item.addEventListener('click', function () {
          autoClose && !openFirst ? closeOther(this) : '';
          openTarget(this);
        });
      });
    }
  }
  function openTarget(item) {
    let content = item.nextElementSibling;
    let display = window.getComputedStyle(content).display;
    content.style.display = display;
    if (display === 'none') {
      display = 'block';
      item.parentNode.classList.add('active');
      item.setAttribute('aria-expanded', 'true');
      content.style.display = 'block';
      let contentHeight = content.scrollHeight;
      content.style.height = '0';
      content.style.transitionProperty = 'height';
      content.style.transitionDuration = `${duration}ms`;
      content.scrollHeight;
      item.querySelector('.accordionState').innerHTML = `${close}`;
      content.style.height = `${contentHeight}px`;
      setTimeout(() => {
        content.style.removeProperty('height');
        content.style.removeProperty('transition-duration');
        content.style.removeProperty('transition-property');
      }, duration);
    } else {
      let contentHeight = content.scrollHeight;
      content.style.height = `${contentHeight}px`;
      content.style.transitionProperty = 'height';
      content.style.transitionDuration = `${duration}ms`;
      content.scrollHeight;
      content.style.height = '0';
      item.querySelector('.accordionState').innerHTML = `${open}`;
      item.parentNode.classList.remove('active');
      item.setAttribute('aria-expanded', 'false');
      setTimeout(() => {
        content.style.removeProperty('height');
        content.style.removeProperty('display');
        content.style.removeProperty('transition-duration');
        content.style.removeProperty('transition-property');
      }, duration);
    }
  }
  function closeOther(item) {
    const siblings = [...item.parentNode.parentNode.children].filter((child) => {
      return child !== item.parentNode;
    });
    siblings.forEach((otherItem, index) => {
      let content = otherItem.querySelector('.accordionContent');
      if (content.style.Height !== 0 || content.style.Height !== null) {
        otherItem.querySelector('.accordionState').innerHTML = `${open}`;
        otherItem.classList.remove('active');
        otherItem.querySelector('.accordionList').setAttribute('aria-expanded', 'false');
        let contentHeight = content.scrollHeight;
        content.style.height = `${contentHeight}px`;
        content.style.transitionProperty = 'height';
        content.style.transitionDuration = `${duration}ms`;
        content.scrollHeight;
        content.style.height = '0';
        setTimeout(() => {
          content.style.removeProperty('height');
          content.style.removeProperty('display');
          content.style.removeProperty('transition-duration');
          content.style.removeProperty('transition-property');
        }, duration);
      }
    });
  }
  (function () {
    clickFunction();
    a11y();
    info();
  })();
}
accordionFunction({
  accordion: '.accordion',
  openFirst: false, // 預設先展開所有內容，使用無障礙遊走不再有手風琴效果，永遠展開內容(滑鼠點擊正常開合)
  autoClose: true, // 若需要此功能需要關閉openFirst
  duration: 200,
  info: {
    open: '展開', // 收合時顯示
    close: '收合', // 展開時顯示
  },
});
</script>
