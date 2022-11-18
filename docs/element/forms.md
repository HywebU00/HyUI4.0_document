# Forms / 表單

?>檔案名稱：sass / module /`form.scss`

---

!> 注意 :zap:表單外層以 `<div class="flexForm"></div>`包覆，css `<form>`上為符合無障礙標準須加上`<label></label>`，但是不想要在畫面上出現文字時，加上 className `labelHidden`隱藏 label 文字

---

## 文字表單

### 預設文字表單

<!-- panels:start -->
<div class="flexForm">
  <label for="username">帳號:</label>
  <input type="text" id="username" placeholder="請輸入文字" />
</div>
<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm">
  <label for="username">帳號:</label>
  <input type="text" id="username" placeholder="請輸入文字" />
</div>
```

<!-- tabs:end -->

### 預設密碼表單

<div class="flexForm">
  <label for="password">密碼:</label>
   <input type="password" name="password" placeholder="請輸入密碼">
</div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm">
  <label for="password">密碼:</label>
  <input type="password" name="password" placeholder="請輸入密碼" />
</div>
```

<!-- tabs:end -->

### 預設組合範例

<div class="flexForm">
    <div class="formGrp">
        <label for="username">帳號:</label>
        <input name="username" type="text" placeholder="請輸入文字">
    </div>
    <div class="formGrp">
        <label for="password">密碼:</label>
        <input name="password" type="password" placeholder="請輸入密碼">
    </div>
    <div class="checkbox">
        <label><input type="checkbox">記住我</label>
    </div>
    <div class="btnGrp formInline">
        <button class="btn btn-reset">清除</button>
        <button class="btn btn-submit">送出</button>
    </div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm">
  <div class="formGrp">
    <label for="username">帳號:</label>
    <input name="username" type="text" placeholder="請輸入文字" />
  </div>
  <div class="formGrp">
    <label for="password">密碼:</label>
    <input name="password" type="password" placeholder="請輸入密碼" />
  </div>
  <div class="checkbox">
    <label><input type="checkbox" />記住我</label>
  </div>
  <div class="btnGrp formInline">
    <button class="btn btn-reset">清除</button>
    <button class="btn btn-submit">送出</button>
  </div>
</div>
```

<!-- tabs:end -->

### 預設組合範例 - 行內設定

加上 className`form_inline`設定行內樣式

<div class="flexForm formInline">
    <div class="formGrp">
        <label for="username">帳號:</label>
        <input name="username" type="text" placeholder="請輸入文字">
    </div>
    <div class="formGrp">
        <label for="password">密碼:</label>
        <div class="input_i">
            <i class="i_lock"></i>
            <input name="password" type="password" placeholder="請輸入密碼">
        </div>
    </div>
    <div class="checkGrp">
        <label><input type="checkbox">記住我</label>
    </div>
    <div class="btnGrp">
        <input name="" type="reset" value="清除" class="btn btnReset">
        <input name="" type="submit" value="送出" class="btn btnSubmit">
    </div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm formInline">
  <div class="formGrp">
    <label for="username">帳號:</label>
    <input name="username" type="text" placeholder="請輸入文字" />
  </div>
  <div class="formGrp">
    <label for="password">密碼:</label>
    <div class="input_i">
      <i class="i_lock"></i>
      <input name="password" type="password" placeholder="請輸入密碼" />
    </div>
  </div>
  <div class="checkGrp">
    <label><input type="checkbox" />記住我</label>
  </div>
  <div class="btnGrp">
    <input name="" type="reset" value="清除" class="btn btnReset" />
    <input name="" type="submit" value="送出" class="btn btnSubmit" />
  </div>
</div>
```

<!-- tabs:end -->

### 多行文字表單

<div class="flexForm">
  <div class="formGrp">
    <label for="textareaSample1">標題</label>
    <textarea id="textareaSample1" rows="3"></textarea>
  </div>
</div>
<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm">
  <div class="formGrp">
    <label for="textareaSample1">標題</label>
    <textarea id="textareaSample1" rows="3"></textarea>
  </div>
</div>
```

<!-- tabs:end -->

### 多行文字表單 - 行內設定

<div class="flexForm">
  <div class="formGrp formInline">
    <label for="textareaSample2">標題</label>
    <textarea id="textareaSample2" rows="3"></textarea>
  </div>
</div>
<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm">
  <div class="formGrp formInline">
    <label for="textareaSample2">標題</label>
    <textarea id="textareaSample2" rows="3"></textarea>
  </div>
</div>
```

<!-- tabs:end -->

## 核取與單選

### 預設核取方塊

<div class="flexForm">
    <div class="checkGrp">
        <label><input type="checkbox" value="">選項一</label>
        <label><input type="checkbox" value="">選項二</label>
        <label><input type="checkbox" value="">選項三</label>
    </div>
</div>
<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm">
  <div class="checkGrp">
    <label><input type="checkbox" value="" />選項一</label>
    <label><input type="checkbox" value="" />選項二</label>
    <label><input type="checkbox" value="" />選項三</label>
  </div>
</div>
```

<!-- tabs:end -->

### 預設核取方塊 - 行內設定

<div class="flexForm">
    <!--最外層的form 或 check_grp class加上form_inline-->
    <div class="checkGrp formInline">
        <label><input name="" type="checkbox" value="">選項一</label>
        <label><input name="" type="checkbox" value="">選項二</label>
        <label><input name="" type="checkbox" value="">選項三</label>
    </div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm">
  <!--最外層的form 或 check_grp class加上form_inline-->
  <div class="checkGrp formInline">
    <label><input name="" type="checkbox" value="" />選項一</label>
    <label><input name="" type="checkbox" value="" />選項二</label>
    <label><input name="" type="checkbox" value="" />選項三</label>
  </div>
</div>
```

<!-- tabs:end -->

### 預設單選方塊

<div class="flexForm">
  <!--最外層的form 或 radio_grp class加上form_inline-->
  <div class="radioGrp formInline">
    <label><input name="radioSample" type="radio" value="" />選項一</label>
    <label><input name="radioSample" type="radio" value="" />選項二</label>
    <label><input name="radioSample" type="radio" value="" />選項三</label>
  </div>
</div>
<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm">
  <!--最外層的form 或 radio_grp class加上form_inline-->
  <div class="radioGrp formInline">
    <label><input name="radioSample" type="radio" value="" />選項一</label>
    <label><input name="radioSample" type="radio" value="" />選項二</label>
    <label><input name="radioSample" type="radio" value="" />選項三</label>
  </div>
</div>
```

<!-- tabs:end -->

### 預設單選方塊 - 行內設定

<div class="flexForm">
  <!--最外層的form 或 radio_grp class加上form_inline-->
  <div class="radioGrp formInline">
    <label><input name="radioSample" type="radio" value="" />選項一</label>
    <label><input name="radioSample" type="radio" value="" />選項二</label>
    <label><input name="radioSample" type="radio" value="" />選項三</label>
  </div>
</div>
<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm">
  <!--最外層的form 或 radio_grp class加上form_inline-->
  <div class="radioGrp formInline">
    <label><input name="radioSample" type="radio" value="" />選項一</label>
    <label><input name="radioSample" type="radio" value="" />選項二</label>
    <label><input name="radioSample" type="radio" value="" />選項三</label>
  </div>
</div>
```

<!-- tabs:end -->

## 下拉選單

<div class="flexForm">
  <div class="formGrp">
    <label for="selectSample">選單</label>
    <select name="" id="selectSample">
      <option value="">選項一</option>
      <option value="">選項二</option>
      <option value="">選項三</option>
      <option value="">選項四</option>
    </select>
  </div>
</div>
<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm">
  <div class="formGrp">
    <label for="selectSample">選單</label>
    <select name="" id="selectSample">
      <option value="">選項一</option>
      <option value="">選項二</option>
      <option value="">選項三</option>
      <option value="">選項四</option>
    </select>
  </div>
</div>
```

<!-- tabs:end -->

### 下拉選單 - 行內設定

<div class="flexForm">
  <div class="formGrp formInline">
    <label for="selectSample">選單</label>
    <select name="" id="selectSample">
      <option value="">選項一</option>
      <option value="">選項二</option>
      <option value="">選項三</option>
      <option value="">選項四</option>
    </select>
  </div>
</div>
<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm">
  <div class="formGrp formInline">
    <label for="selectSample">選單</label>
    <select name="" id="selectSample">
      <option value="">選項一</option>
      <option value="">選項二</option>
      <option value="">選項三</option>
      <option value="">選項四</option>
    </select>
  </div>
</div>
```

<!-- tabs:end -->

## 檔案瀏覽 or 上傳檔案

### 單個檔案上傳

<div class="flexForm">
  <div class="uploadGrp">
    <input class="upload_file" type="text" readonly />
    <div class="uploadBtn">
      <span>上傳檔案</span>
      <input type="file" class="check_file" />
    </div>
  </div>
</div>
<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm">
  <div class="uploadGrp">
    <input class="upload_file" type="text" readonly />
    <div class="uploadBtn">
      <span>上傳檔案</span>
      <input type="file" class="check_File" />
    </div>
  </div>
</div>
```

#### **JavaScript**

```javascript
function addFile() {
  const addFileName = document.querySelectorAll('.check_file');
  addFileName.forEach((i) => {
    i.addEventListener('change', pushFileName);
  });

  function pushFileName(e) {
    let _fileLen = e.target.files.length;
    let _fileName = '';
    const uploadInput = e.target.parentNode.closest('.uploadGrp').querySelector('.upload_file');
    if (_fileLen > 1) {
      _fileName = `${_fileLen} files selected`;
    } else {
      _fileName = e.target.files[0].name;
    }
    uploadInput.value = _fileName;
  }
}
addFile();
```

<!-- tabs:end -->

### 多個檔案上傳

<div class="flexForm">
  <div class="uploadGrp">
    <input class="upload_file" type="text" readonly />
    <div class="uploadBtn">
      <span>上傳多個檔案</span>
      <input type="file" class="check_file" multiple />
    </div>
  </div>
</div>
<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm">
  <div class="uploadGrp">
    <input class="upload_file" type="text" readonly />
    <div class="uploadBtn">
      <span>上傳多個檔案</span>
      <input type="file" class="check_file" multiple />
    </div>
  </div>
</div>
```

#### **JavaScript**

```javascript
function addFile() {
  const addFileName = document.querySelectorAll('.check_file');
  addFileName.forEach((i) => {
    i.addEventListener('change', pushFileName);
  });

  function pushFileName(e) {
    let _fileLen = e.target.files.length;
    let _fileName = '';
    const uploadInput = e.target.parentNode.closest('.uploadGrp').querySelector('.upload_file');
    if (_fileLen > 1) {
      _fileName = `${_fileLen} files selected`;
    } else {
      _fileName = e.target.files[0].name;
    }
    uploadInput.value = _fileName;
  }
}
addFile();
```

<!-- tabs:end -->

## 有 Icon 的 input

在需帶有 icon 的`input`外層包覆`<div class="input-i"></div>`

<div class="flexForm">
  <div class="input_i">
    <i class="i_lock"></i>
    <input name="password" type="password" placeholder="請輸入密碼">
  </div>
  <div class="input_i">
    <input name="email" type="email" id="email">
    <i class="i_mail"></i>
  </div>
</div>
<!-- tabs:start -->
#### **HTML**

```html
<div class="flexForm">
  <div class="input_i">
    <i class="i_lock"></i>
    <input name="password" type="password" placeholder="請輸入密碼" />
  </div>
  <div class="input_i">
    <input name="email" type="email" id="email" />
    <i class="i_mail"></i>
  </div>
</div>
```

<!-- tabs:end -->

## 表單排版範例

### 格線式表單

<div class="flexForm formGrid">
    <div class="formGrp">
        <label for="username" class="formTitle">帳號<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></label>
        <div class="formContent">
            <div class="input_i">
                <i class="i_man"></i>
                <input type="text" id="username" value="readonly or disable" readonly="">
            </div>
            <div class="help">說明文字</div>
        </div>
    </div>
    <div class="formGrp">
        <label for="password" class="formTitle">密碼<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></label>
        <div class="formContent">
            <div class="input_i">
                <i class="i_lock"></i>
                <input name="password" type="password" placeholder="請輸入密碼">
            </div>
            <div class="noticeError">您輸入的帳號密碼有誤！</div>
        </div>
    </div>
    <div class="formGrp">
        <label for="email" class="formTitle">E-mail<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></label>
        <div class="formContent">
            <div class="input_i">
                <input name="email" type="email" id="email">
                <i class="i_mail"></i>
            </div>
            <div class="notice">這是一般提醒訊息區塊</div>
            <div class="noticeWarning">這似乎不是一個正常的Email格式 <a href="#" class="close"><img src="images/basic/icon_close.svg" alt=""></a>
            </div>
        </div>
    </div>
    <div class="formGrp">
        <label for="phone" class="formTitle">手機號碼<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></label>
        <div class="formContent">
            <input name="phone" id="phone" type="tel">
        </div>
    </div>
    <div class="formGrp">
        <div class="formTitle">起始日期(type="date")</div>
        <div class="formContent">
            <div class="datepick">
                <input name="" type="date" value="" class="calendar" placeholder="開始日期">
            </div>
            <div class="datepick">
                <input name="" type="date" value="" class="calendar" placeholder="結束日期">
            </div>
        </div>
    </div>
    <div class="formGrp">
        <label for="address" class="formTitle">活動名稱</label>
        <div class="formContent">
            <input name="password" type="password">
        </div>
    </div>
    <div class="formGrp" role="group" aria-labelledby="fake-legend">
        <div for="" class="formTitle">活動地點</div>
        <div class="formContent" id="fake-legend">
            <div class="radioGrp formInline">
                <label>
                    <input type="radio" name="sampleRadio5" value="" checked="">新北市</label>
                <label>
                    <input type="radio" name="sampleRadio5" value="">臺北市</label>
                <label>
                    <input type="radio" name="sampleRadio5" value="">臺中市</label>
                <label>
                    <input type="radio" name="sampleRadio5" value="">臺南市</label>
                <label>
                    <input type="radio" name="sampleRadio5" value="">高雄市</label>
                <label>
                    <input type="radio" name="sampleRadio5" value="">宜蘭縣</label>
                <label>
                    <input type="radio" name="sampleRadio5" value="">新竹縣</label>
            </div>
        </div>
    </div>
    <div class="formGrp">
        <label for="address" class="formTitle">詳細地址</label>
        <div class="formContent">
            <textarea name="" id="address" cols="30" rows="10"></textarea>
        </div>
    </div>
    <div class="formGrp" role="group" aria-labelledby="fake-legend">
        <label class="formTitle">活動地點</label>
        <div class="formContent" id="fake-legend">
            <div class="checkGrp formInline">
                <label>
                    <input type="checkbox" name="" value="" checked="">全部</label>
                <label>
                    <input type="checkbox" name="" value="">展覽</label>
                <label>
                    <input type="checkbox" name="" value="">表演與節慶</label>
                <label>
                    <input type="checkbox" name="" value="">演講／講座／研討會</label>
                <label>
                    <input type="checkbox" name="" value="">綜合</label>
            </div>
        </div>
    </div>
    <div class="formGrp">
        <label for="selectSample" class="formTitle">選單 (inline)</label>
        <div class="formContent formInline">
            <select id="selectSample" name="">
                <option value="">全部</option>
                <option value="">視覺藝術（藝術品與美術）</option>
                <option value="">工藝（不含古物、古董）</option>
                <option value="">設計</option>
                <option value="">古典與傳統音樂</option>
                <option value="">流行音樂</option>
                <option value="">戲劇</option>
                <option value="">舞蹈</option>
            </select>
        </div>
    </div>
    <div class="formGrp">
        <label for="selectSample" class="formTitle">選單</label>
        <div class="formContent">
            <select id="selectSample" name="">
                <option value="">全部</option>
                <option value="">視覺藝術（藝術品與美術）</option>
                <option value="">工藝（不含古物、古董）</option>
                <option value="">設計</option>
                <option value="">古典與傳統音樂</option>
                <option value="">流行音樂</option>
                <option value="">戲劇</option>
                <option value="">舞蹈</option>
            </select>
        </div>
    </div>
    <div class="formGrp" role="group" aria-labelledby="fake-legend">
        <label class="formTitle">是否售票</label>
        <div class="formContent" id="fake-legend">
            <div class="radioGrp formInline">
                <label>
                    <input type="radio" name="sampleRadio6" value="" checked="">售票</label>
                <label>
                    <input type="radio" name="sampleRadio6" value="">免費索票</label>
                <label>
                    <input type="radio" name="sampleRadio6" value="">自由入場</label>
            </div>
        </div>
    </div>
    <div class="formGrp">
        <label for="" class="formTitle">有條件式表單</label>
        <div class="formContent additional">
            <div class="checkbox">
                <label><input name="checkSample" type="checkbox" value=""><span>同會員資訊</span></label>
            </div>
            <input type="text" name="">
        </div>
    </div>
    <div class="formGrp">
        <label for="" class="formTitle">單檔上傳</label>
        <div class="formContent">
            <div class="uploadGrp">
                <input class="upload_file" type="text" readonly="">
                <div class="uploadBtn">
                    <span>上傳檔案</span>
                    <input type="file" class="check_file">
                </div>
            </div>
        </div>
    </div>
    <div class="formGrp">
        <label for="" class="formTitle">多檔上傳</label>
        <div class="formContent">
            <div class="uploadGrp">
                <input class="upload_file" type="text" readonly="">
                <div class="uploadBtn">
                    <span>上傳多個檔案</span>
                    <input type="file" class="check_file" multiple="">
                </div>
            </div>
        </div>
    </div>
    <div class="btnGrp formInline">
        <button class="btn btnReset">清除</button>
        <button class="btn btnSubmit">送出</button>
    </div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm formGrid">
  <div class="formGrp">
    <label for="username" class="formTitle">帳號<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></label>
    <div class="formContent">
      <div class="input_i">
        <i class="i_man"></i>
        <input type="text" id="username" value="readonly or disable" readonly="" />
      </div>
      <div class="help">說明文字</div>
    </div>
  </div>
  <div class="formGrp">
    <label for="password" class="formTitle">密碼<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></label>
    <div class="formContent">
      <div class="input_i">
        <i class="i_lock"></i>
        <input name="password" type="password" placeholder="請輸入密碼" />
      </div>
      <div class="noticeError">您輸入的帳號密碼有誤！</div>
    </div>
  </div>
  <div class="formGrp">
    <label for="email" class="formTitle">E-mail<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></label>
    <div class="formContent">
      <div class="input_i">
        <input name="email" type="email" id="email" />
        <i class="i_mail"></i>
      </div>
      <div class="notice">這是一般提醒訊息區塊</div>
      <div class="noticeWarning">
        這似乎不是一個正常的Email格式 <a href="#" class="close"><img src="images/basic/icon_close.svg" alt="" /></a>
      </div>
    </div>
  </div>
  <div class="formGrp">
    <label for="phone" class="formTitle">手機號碼<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></label>
    <div class="formContent">
      <input name="phone" id="phone" type="tel" />
    </div>
  </div>
  <div class="formGrp">
    <div class="formTitle">起始日期(type="date")</div>
    <div class="formContent">
      <div class="datepick">
        <input name="" type="date" value="" class="calendar" placeholder="開始日期" />
      </div>
      <div class="datepick">
        <input name="" type="date" value="" class="calendar" placeholder="結束日期" />
      </div>
    </div>
  </div>
  <div class="formGrp">
    <label for="address" class="formTitle">活動名稱</label>
    <div class="formContent">
      <input name="password" type="password" />
    </div>
  </div>
  <div class="formGrp" role="group" aria-labelledby="fake-legend">
    <div for="" class="formTitle">活動地點</div>
    <div class="formContent" id="fake-legend">
      <div class="radioGrp formInline">
        <label> <input type="radio" name="sampleRadio5" value="" checked="" />新北市</label>
        <label> <input type="radio" name="sampleRadio5" value="" />臺北市</label>
        <label> <input type="radio" name="sampleRadio5" value="" />臺中市</label>
        <label> <input type="radio" name="sampleRadio5" value="" />臺南市</label>
        <label> <input type="radio" name="sampleRadio5" value="" />高雄市</label>
        <label> <input type="radio" name="sampleRadio5" value="" />宜蘭縣</label>
        <label> <input type="radio" name="sampleRadio5" value="" />新竹縣</label>
      </div>
    </div>
  </div>
  <div class="formGrp">
    <label for="address" class="formTitle">詳細地址</label>
    <div class="formContent">
      <textarea name="" id="address" cols="30" rows="10"></textarea>
    </div>
  </div>
  <div class="formGrp" role="group" aria-labelledby="fake-legend">
    <label class="formTitle">活動地點</label>
    <div class="formContent" id="fake-legend">
      <div class="checkGrp formInline">
        <label> <input type="checkbox" name="" value="" checked="" />全部</label>
        <label> <input type="checkbox" name="" value="" />展覽</label>
        <label> <input type="checkbox" name="" value="" />表演與節慶</label>
        <label> <input type="checkbox" name="" value="" />演講／講座／研討會</label>
        <label> <input type="checkbox" name="" value="" />綜合</label>
      </div>
    </div>
  </div>
  <div class="formGrp">
    <label for="selectSample" class="formTitle">選單 (inline)</label>
    <div class="formContent formInline">
      <select id="selectSample" name="">
        <option value="">全部</option>
        <option value="">視覺藝術（藝術品與美術）</option>
        <option value="">工藝（不含古物、古董）</option>
        <option value="">設計</option>
        <option value="">古典與傳統音樂</option>
        <option value="">流行音樂</option>
        <option value="">戲劇</option>
        <option value="">舞蹈</option>
      </select>
    </div>
  </div>
  <div class="formGrp">
    <label for="selectSample" class="formTitle">選單</label>
    <div class="formContent">
      <select id="selectSample" name="">
        <option value="">全部</option>
        <option value="">視覺藝術（藝術品與美術）</option>
        <option value="">工藝（不含古物、古董）</option>
        <option value="">設計</option>
        <option value="">古典與傳統音樂</option>
        <option value="">流行音樂</option>
        <option value="">戲劇</option>
        <option value="">舞蹈</option>
      </select>
    </div>
  </div>
  <div class="formGrp" role="group" aria-labelledby="fake-legend">
    <label class="formTitle">是否售票</label>
    <div class="formContent" id="fake-legend">
      <div class="radioGrp formInline">
        <label> <input type="radio" name="sampleRadio6" value="" checked="" />售票</label>
        <label> <input type="radio" name="sampleRadio6" value="" />免費索票</label>
        <label> <input type="radio" name="sampleRadio6" value="" />自由入場</label>
      </div>
    </div>
  </div>
  <div class="formGrp">
    <label for="" class="formTitle">有條件式表單</label>
    <div class="formContent additional">
      <div class="checkbox">
        <label><input name="checkSample" type="checkbox" value="" /><span>同會員資訊</span></label>
      </div>
      <input type="text" name="" />
    </div>
  </div>
  <div class="formGrp">
    <label for="" class="formTitle">單檔上傳</label>
    <div class="formContent">
      <div class="uploadGrp">
        <input class="upload_file" type="text" readonly="" />
        <div class="uploadBtn">
          <span>上傳檔案</span>
          <input type="file" class="check_file" />
        </div>
      </div>
    </div>
  </div>
  <div class="formGrp">
    <label for="" class="formTitle">多檔上傳</label>
    <div class="formContent">
      <div class="uploadGrp">
        <input class="upload_file" type="text" readonly="" />
        <div class="uploadBtn">
          <span>上傳多個檔案</span>
          <input type="file" class="check_file" multiple="" />
        </div>
      </div>
    </div>
  </div>
  <div class="btnGrp formInline">
    <button class="btn btnReset">清除</button>
    <button class="btn btnSubmit">送出</button>
  </div>
</div>
```

<!-- tabs:end -->

<!-- <iframe height="500" style="width: 100%;" scrolling="no" title="格線式表單" src="https://codepen.io/u00hyui/embed/poeXBVL?defaultTab=html%2Cresult&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/u00hyui/pen/poeXBVL">
  格線式表單</a> by u00hyui (<a href="https://codepen.io/u00hyui">@u00hyui</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe> -->

### 多欄、格線式表單 1

<div class="formGrid flexForm">
    <div class="formGrp">
        <div class="formTitle">formCol_6_6</div>
        <div class="formContent formCol_6_6">
            <label for="inputSample" class="labelHidden">雙欄1</label>
            <input name="username" id="inputSample" type="text">
            <label for="inputSample2" class="labelHidden">雙欄2</label>
            <input name="username" id="inputSample2" type="text">
            <div class="notice">加上className "labelHidden" 隱藏label文字</div>
        </div>
    </div>
    <div class="formGrp">
        <div class="formTitle">formCol_4_4_4</div>
        <div class="formContent formCol_4_4_4">
            <input name="username" type="text">
            <input name="username" type="text">
            <select id="selectSample" name="">
                <option value="">全部</option>
                <option value="">視覺藝術（藝術品與美術）</option>
                <option value="">工藝（不含古物、古董）</option>
                <option value="">設計</option>
                <option value="">古典與傳統音樂</option>
                <option value="">流行音樂</option>
                <option value="">戲劇</option>
                <option value="">舞蹈</option>
            </select>
        </div>
    </div>
    <div class="formGrp">
        <div class="formTitle">formCol_3_3_3_3</div>
        <div class="formContent formCol_3_3_3_3">
            <input name="username" type="text">
            <input name="username" type="text">
            <input name="username" type="text">
            <label><input name="radioSample" type="radio" value=""><span>選項</span></label>
        </div>
    </div>
    <div class="formGrp">
        <div class="formTitle">formCol_2_2_2_2_2_2</div>
        <div class="formContent formCol_2_2_2_2_2_2">
            <input name="username" type="text">
            <input name="username" type="text">
            <input name="username" type="text">
            <input name="username" type="text">
            <input name="username" type="text">
            <label><input name="radioSample" type="radio" value=""><span>選項</span></label>
        </div>
    </div>
    <div class="formGrp">
        <div class="formTitle">formCol_3_9</div>
        <div class="formContent formCol_3_9 ">
            <input name="username" type="text">
            <input name="username" type="text">
        </div>
    </div>
    <div class="formGrp">
        <div class="formTitle">formCol_3_3_6</div>
        <div class="formContent formCol_3_3_6">
            <select name="" id="">
                <option value="">台北市</option>
                <option value="">新北市</option>
                <option value="">桃園市</option>
                <option value="">新竹市</option>
                <option value="">...</option>
            </select>
            <select name="" id="">
                <option value="">中正區</option>
                <option value="">大安區</option>
                <option value="">信義區</option>
                <option value="">北投區</option>
                <option value="">...</option>
            </select>
            <input name="username" type="text">
        </div>
    </div>
    <div class="formGrp">
        <div class="formTitle">formCol_9_3</div>
        <div class="formContent formCol_9_3">
            <input name="username" type="text">
            <input name="username" type="text">
        </div>
    </div>
    <div class="formGrp">
        <div class="formTitle">formCol_4_8</div>
        <div class="formContent formCol_4_8">
            <input name="username" type="text">
            <input name="username" type="text">
        </div>
    </div>
    <div class="formGrp">
        <div class="formTitle">formCol_2_10</div>
        <div class="formContent formCol_2_10">
            <input name="username" type="text">
            <input name="username" type="text">
        </div>
    </div>
    <div class="formGrp">
        <div class="formTitle">formCol_2_2_8</div>
        <div class="formContent formCol_2_2_8">
            <select name="" id="">
                <option value="">台北市</option>
                <option value="">新北市</option>
                <option value="">桃園市</option>
                <option value="">新竹市</option>
                <option value="">...</option>
            </select>
            <select name="" id="">
                <option value="">中正區</option>
                <option value="">大安區</option>
                <option value="">信義區</option>
                <option value="">北投區</option>
                <option value="">...</option>
            </select>
            <input name="username" type="text">
        </div>
    </div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="formGrid flexForm">
  <div class="formGrp">
    <div class="formTitle">formCol_6_6</div>
    <div class="formContent formCol_6_6">
      <label for="inputSample" class="labelHidden">雙欄1</label>
      <input name="username" id="inputSample" type="text" />
      <label for="inputSample2" class="labelHidden">雙欄2</label>
      <input name="username" id="inputSample2" type="text" />
      <div class="notice">加上className "labelHidden" 隱藏label文字</div>
    </div>
  </div>
  <div class="formGrp">
    <div class="formTitle">formCol_4_4_4</div>
    <div class="formContent formCol_4_4_4">
      <input name="username" type="text" />
      <input name="username" type="text" />
      <select id="selectSample" name="">
        <option value="">全部</option>
        <option value="">視覺藝術（藝術品與美術）</option>
        <option value="">工藝（不含古物、古董）</option>
        <option value="">設計</option>
        <option value="">古典與傳統音樂</option>
        <option value="">流行音樂</option>
        <option value="">戲劇</option>
        <option value="">舞蹈</option>
      </select>
    </div>
  </div>
  <div class="formGrp">
    <div class="formTitle">formCol_3_3_3_3</div>
    <div class="formContent formCol_3_3_3_3">
      <input name="username" type="text" />
      <input name="username" type="text" />
      <input name="username" type="text" />
      <label><input name="radioSample" type="radio" value="" /><span>選項</span></label>
    </div>
  </div>
  <div class="formGrp">
    <div class="formTitle">formCol_2_2_2_2_2_2</div>
    <div class="formContent formCol_2_2_2_2_2_2">
      <input name="username" type="text" />
      <input name="username" type="text" />
      <input name="username" type="text" />
      <input name="username" type="text" />
      <input name="username" type="text" />
      <label><input name="radioSample" type="radio" value="" /><span>選項</span></label>
    </div>
  </div>
  <div class="formGrp">
    <div class="formTitle">formCol_3_9</div>
    <div class="formContent formCol_3_9 ">
      <input name="username" type="text" />
      <input name="username" type="text" />
    </div>
  </div>
  <div class="formGrp">
    <div class="formTitle">formCol_3_3_6</div>
    <div class="formContent formCol_3_3_6">
      <select name="" id="">
        <option value="">台北市</option>
        <option value="">新北市</option>
        <option value="">桃園市</option>
        <option value="">新竹市</option>
        <option value="">...</option>
      </select>
      <select name="" id="">
        <option value="">中正區</option>
        <option value="">大安區</option>
        <option value="">信義區</option>
        <option value="">北投區</option>
        <option value="">...</option>
      </select>
      <input name="username" type="text" />
    </div>
  </div>
  <div class="formGrp">
    <div class="formTitle">formCol_9_3</div>
    <div class="formContent formCol_9_3">
      <input name="username" type="text" />
      <input name="username" type="text" />
    </div>
  </div>
  <div class="formGrp">
    <div class="formTitle">formCol_4_8</div>
    <div class="formContent formCol_4_8">
      <input name="username" type="text" />
      <input name="username" type="text" />
    </div>
  </div>
  <div class="formGrp">
    <div class="formTitle">formCol_2_10</div>
    <div class="formContent formCol_2_10">
      <input name="username" type="text" />
      <input name="username" type="text" />
    </div>
  </div>
  <div class="formGrp">
    <div class="formTitle">formCol_2_2_8</div>
    <div class="formContent formCol_2_2_8">
      <select name="" id="">
        <option value="">台北市</option>
        <option value="">新北市</option>
        <option value="">桃園市</option>
        <option value="">新竹市</option>
        <option value="">...</option>
      </select>
      <select name="" id="">
        <option value="">中正區</option>
        <option value="">大安區</option>
        <option value="">信義區</option>
        <option value="">北投區</option>
        <option value="">...</option>
      </select>
      <input name="username" type="text" />
    </div>
  </div>
</div>
```

<!-- tabs:end -->

### 多欄、格線式表單 2

<div class="formGrid flexForm">
  <div class="formGrp">
    <div class="formTitle">第一層Title</div>
    <div class="formContent">
        <!-- 二欄 -->
        <div class="formGrp">
            <div class="formContent formCol_6_6">
                <div class="formGrp">
                    <label for="username" class="formTitle">雙欄 欄目Ａ：</label>
                    <div class="input_i">
                        <input name="username" type="text">
                        <i class="i_lock"></i>
                    </div>
                </div>
                <div class="formGrp">
                    <label for="username" class="formTitle">雙欄 欄目B：</label>
                    <input name="username" type="text">
                </div>
                <div class="formGrp">
                    <label for="username" class="formTitle">雙欄 欄目C：</label>
                    <select name="" id="">
                        <option value="">台北市</option>
                        <option value="">新北市</option>
                        <option value="">桃園市</option>
                        <option value="">新竹市</option>
                        <option value="">...</option>
                    </select>
                </div>
                <div class="formGrp">
                    <label for="username" class="formTitle">雙欄 欄目D：</label>
                    <select name="" id="" disabled="">
                        <option value="">台北市</option>
                        <option value="">新北市</option>
                        <option value="">桃園市</option>
                        <option value="">新竹市</option>
                        <option value="">...</option>
                    </select>
                </div>
            </div>
        </div>
        <!-- 三欄 -->
        <div class="formGrp">
            <div class="formContent formCol_4_4_4">
                <div class="formGrp">
                    <label for="username" class="formTitle">三欄 欄目A：</label>
                    <input name="username" type="text">
                </div>
                <div class="formGrp">
                    <label for="username" class="formTitle">三欄 欄目B：</label>
                    <select name="" id="" disabled="">
                        <option value="">台北市</option>
                        <option value="">新北市</option>
                        <option value="">桃園市</option>
                        <option value="">新竹市</option>
                        <option value="">...</option>
                    </select>
                </div>
                <div class="formGrp">
                    <label for="username" class="formTitle">三欄 欄目C：</label>
                    <select name="" id="">
                        <option value="">台北市</option>
                        <option value="">新北市</option>
                        <option value="">桃園市</option>
                        <option value="">新竹市</option>
                        <option value="">...</option>
                    </select>
                </div>
            </div>
        </div>
        <!-- 四欄 -->
        <div class="formGrp">
            <div class="formContent formCol_3_3_3_3">
                <div class="formGrp">
                    <label for="username" class="formTitle">四欄 欄目A：</label>
                    <input name="username" type="text" placeholder="請輸入人數">
                </div>
                <div class="formGrp">
                    <label for="username" class="formTitle">四欄 欄目B：</label>
                    <select name="" id="" disabled="">
                        <option value="">台北市</option>
                        <option value="">新北市</option>
                        <option value="">桃園市</option>
                        <option value="">新竹市</option>
                        <option value="">...</option>
                    </select>
                </div>
                <div class="formGrp">
                    <label for="username" class="formTitle">四欄 欄目C：</label>
                    <select name="" id="">
                        <option value="">台北市</option>
                        <option value="">新北市</option>
                        <option value="">桃園市</option>
                        <option value="">新竹市</option>
                        <option value="">...</option>
                    </select>
                </div>
                <div class="formGrp">
                    <label for="username" class="formTitle">四欄 欄目D：</label>
                    <input name="username" type="text" value="0" placeholder="" readonly="">
                </div>
            </div>
        </div>
    </div>
</div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="formGrid flexForm">
  <div class="formGrp">
    <div class="formTitle">第一層Title</div>
    <div class="formContent">
      <!-- 二欄 -->
      <div class="formGrp">
        <div class="formContent formCol_6_6">
          <div class="formGrp">
            <label for="username" class="formTitle">雙欄 欄目Ａ：</label>
            <div class="input_i">
              <input name="username" type="text" />
              <i class="i_lock"></i>
            </div>
          </div>
          <div class="formGrp">
            <label for="username" class="formTitle">雙欄 欄目B：</label>
            <input name="username" type="text" />
          </div>
          <div class="formGrp">
            <label for="username" class="formTitle">雙欄 欄目C：</label>
            <select name="" id="">
              <option value="">台北市</option>
              <option value="">新北市</option>
              <option value="">桃園市</option>
              <option value="">新竹市</option>
              <option value="">...</option>
            </select>
          </div>
          <div class="formGrp">
            <label for="username" class="formTitle">雙欄 欄目D：</label>
            <select name="" id="" disabled="">
              <option value="">台北市</option>
              <option value="">新北市</option>
              <option value="">桃園市</option>
              <option value="">新竹市</option>
              <option value="">...</option>
            </select>
          </div>
        </div>
      </div>
      <!-- 三欄 -->
      <div class="formGrp">
        <div class="formContent formCol_4_4_4">
          <div class="formGrp">
            <label for="username" class="formTitle">三欄 欄目A：</label>
            <input name="username" type="text" />
          </div>
          <div class="formGrp">
            <label for="username" class="formTitle">三欄 欄目B：</label>
            <select name="" id="" disabled="">
              <option value="">台北市</option>
              <option value="">新北市</option>
              <option value="">桃園市</option>
              <option value="">新竹市</option>
              <option value="">...</option>
            </select>
          </div>
          <div class="formGrp">
            <label for="username" class="formTitle">三欄 欄目C：</label>
            <select name="" id="">
              <option value="">台北市</option>
              <option value="">新北市</option>
              <option value="">桃園市</option>
              <option value="">新竹市</option>
              <option value="">...</option>
            </select>
          </div>
        </div>
      </div>
      <!-- 四欄 -->
      <div class="formGrp">
        <div class="formContent formCol_3_3_3_3">
          <div class="formGrp">
            <label for="username" class="formTitle">四欄 欄目A：</label>
            <input name="username" type="text" placeholder="請輸入人數" />
          </div>
          <div class="formGrp">
            <label for="username" class="formTitle">四欄 欄目B：</label>
            <select name="" id="" disabled="">
              <option value="">台北市</option>
              <option value="">新北市</option>
              <option value="">桃園市</option>
              <option value="">新竹市</option>
              <option value="">...</option>
            </select>
          </div>
          <div class="formGrp">
            <label for="username" class="formTitle">四欄 欄目C：</label>
            <select name="" id="">
              <option value="">台北市</option>
              <option value="">新北市</option>
              <option value="">桃園市</option>
              <option value="">新竹市</option>
              <option value="">...</option>
            </select>
          </div>
          <div class="formGrp">
            <label for="username" class="formTitle">四欄 欄目D：</label>
            <input name="username" type="text" value="0" placeholder="" readonly="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```

<!-- tabs:end -->

### 多層次表單

<div class="flexForm formGrid">
    <div class="formGrp">
        <div class="formTitle">個人資料<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></div>
        <div class="formContent">
            <div class="formGrp">
                <label for="" class="formTitle">姓名<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></label>
                <div class="formContent">
                    <input name="" type="text" value="">
                </div>
            </div>
            <div class="formGrp" role="group" aria-labelledby="fake-legend">
                <label class="formTitle">性別<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></label>
                <div class="formContent" id="fake-legend">
                    <div class="radioGrp formInline">
                        <label>
                            <input type="radio" name="sampleRadio5" value="" checked="">男</label>
                        <label>
                            <input type="radio" name="sampleRadio5" value="">女</label>
                    </div>
                </div>
            </div>
            <div class="formGrp">
                <div class="formTitle">出生年月日<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></div>
                <div class="formContent formInline birthday">
                    <select name="" id="">
                        <option value="">2019</option>
                        <option value="">2018</option>
                        <option value="">2017</option>
                        <option value="">2016</option>
                        <option value="">...</option>
                    </select>年 <select name="" id="">
                        <option value="">01</option>
                        <option value="">02</option>
                        <option value="">03</option>
                        <option value="">04</option>
                        <option value="">...</option>
                    </select>月 <select name="" id="">
                        <option value="">01</option>
                        <option value="">02</option>
                        <option value="">03</option>
                        <option value="">04</option>
                        <option value="">...</option>
                    </select>日 </div>
            </div>
        </div>
    </div>
    <div class="formGrp">
        <div class="formTitle">聯絡方式</div>
        <div class="formContent">
            <div class="formGrp">
                <label for="selectSample" class="formTitle">國家區域</label>
                <div class="formContent formInline">
                    <select id="selectSample" name="">
                        <option value="">台灣</option>
                        <option value="">日本</option>
                        <option value="">美國</option>
                        <option value="">澳洲</option>
                        <option value="">新加坡</option>
                        <option value="">中國大陸</option>
                    </select>
                </div>
            </div>
            <div class="formGrp">
                <label for="" class="formTitle">手機號碼</label>
                <div class="formContent formInline ">
                    <input name="" type="tel" value="" placeholder="0912345678">
                </div>
            </div>
            <div class="formGrp">
                <label for="" class="formTitle">電話號碼</label>
                <div class="formContent formInline tel">
                    <input name="" type="tel" value="" placeholder="886">
                    <input name="" type="tel" value="" placeholder="12345678">
                </div>
            </div>
            <div class="formGrp">
                <label for="" class="formTitle">傳真號碼</label>
                <div class="formContent formInline tel">
                    <input name="" type="tel" value="" placeholder="886">
                    <input name="" type="tel" value="" placeholder="12345678">
                </div>
            </div>
            <div class="formGrp">
                <label for="" class="formTitle">聯絡地址</label>
                <div class="formContent formInline address">
                    <select name="" id="">
                        <option value="">台北市</option>
                        <option value="">新北市</option>
                        <option value="">桃園市</option>
                        <option value="">新竹市</option>
                        <option value="">...</option>
                    </select>
                    <select name="" id="">
                        <option value="">中正區</option>
                        <option value="">大安區</option>
                        <option value="">信義區</option>
                        <option value="">北投區</option>
                        <option value="">...</option>
                    </select>
                    <input name="" type="text" value="">
                </div>
            </div>
            <div class="formGrp">
                <div for="" class="formTitle">寄送地址</div>
                <div class="formContent formInline address">
                    <label for="" class="labelHidden">縣市</label>
                    <select name="" id="">
                        <option value="">台北市</option>
                        <option value="">新北市</option>
                        <option value="">桃園市</option>
                        <option value="">新竹市</option>
                        <option value="">...</option>
                    </select>
                    <label for="" class="labelHidden">行政區域</label>
                    <select name="" id="">
                        <option value="">中正區</option>
                        <option value="">大安區</option>
                        <option value="">信義區</option>
                        <option value="">北投區</option>
                        <option value="">...</option>
                    </select>
                    <label for="" class="labelHidden">詳細地址</label>
                    <input name="" type="text" value="">
                    <div class="checkbox">
                        <label><input type="checkbox">同上聯絡地址</label>
                    </div>
                </div>
            </div>
            <div class="formGrp">
                <label for="" class="formTitle">公司網站</label>
                <div class="formContent">
                    <input name="" type="text" value="">
                </div>
            </div>
            <div class="formGrp">
                <label for="" class="formTitle">網站URL</label>
                <div class="formContent formInline">
                    <select id="selectSample" name="">
                        <option value="">http</option>
                        <option value="">https</option>
                    </select>
                    <input type="text" value="" placeholder="www.hyweb.com.tw">
                </div>
            </div>
        </div>
    </div>
    <div class="formGrp">
        <div class="formTitle">參加活動</div>
        <div class="formContent">
            <div class="formGrp">
                <div class="formTitle"> 起始日期 </div>
                <div class="formContent">
                    <div class="datepick">
                        <input name="" type="text" value="" class="calendar" placeholder="開始日期">
                        <i class="i_calendar"></i>
                    </div>
                    <div class="datepick">
                        <input name="" type="text" value="" class="calendar" placeholder="結束日期">
                        <i class="i_calendar"></i>
                    </div>
                </div>
            </div>
            <div class="formGrp" role="group" aria-labelledby="fake-legend">
                <label class="formTitle">參加場次</label>
                <div class="formContent" id="fake-legend">
                    <div class="checkGrp formInline">
                        <label>
                            <input type="checkbox" name="" value="" checked="">全部</label>
                        <label>
                            <input type="checkbox" name="" value="">展覽</label>
                        <label>
                            <input type="checkbox" name="" value="">表演與節慶</label>
                        <label>
                            <input type="checkbox" name="" value="">演講／講座／研討會</label>
                        <label>
                            <input type="checkbox" name="" value="">綜合</label>
                    </div>
                </div>
            </div>
            <div class="formGrp">
                <div class="formTitle">有微動態</div>
                <div class="formContent">
                    <div class="radioRrp formInline">
                        <label><input name="radioSample" type="radio" value=""><span>選項一</span></label>
                        <label><input name="radioSample" type="radio" value=""><span>選項二</span></label>
                        <label><input name="radioSample" type="radio" value=""><span>其他</span><input type="text"></label>
                    </div>
                </div>
            </div>
            <div class="formGrp">
                <div class="formTitle">有微動態</div>
                <div class="formContent">
                    <div class="checkGrp formInline">
                        <label><input name="" type="checkbox" value=""><span>選項一</span></label>
                        <label><input name="" type="checkbox" value=""><span>選項二</span></label>
                        <label><input name="" type="checkbox" value=""><span>選項三</span></label>
                    </div>
                </div>
            </div>
            <div class="formGrp" role="group" aria-labelledby="fake-legend">
                <label class="formTitle">參加場次</label>
                <div class="formContent" id="fake-legend">
                    <div class="checkGrp">
                        <label>
                            <input type="checkbox" name="" value="" checked="">全部</label>
                        <label>
                            <input type="checkbox" name="" value="">展覽</label>
                        <label>
                            <input type="checkbox" name="" value="">表演與節慶</label>
                        <label>
                            <input type="checkbox" name="" value="">演講／講座／研討會</label>
                        <label>
                            <input type="checkbox" name="" value="">綜合</label>
                    </div>
                </div>
            </div>
            <div class="formGrp" role="group" aria-labelledby="fake-legend">
                <legend class="formTitle">是否售票</legend>
                <div class="formContent" id="fake-legend">
                    <div class="radioGrp formInline">
                        <label>
                            <input type="radio" name="sampleRadio6" value="" checked="">售票</label>
                        <label>
                            <input type="radio" name="sampleRadio6" value="">免費索票</label>
                        <label>
                            <input type="radio" name="sampleRadio6" value="">自由入場</label>
                    </div>
                </div>
            </div>
            <div class="formGrp" role="group" aria-labelledby="fake-legend">
                <label class="formTitle">是否售票</label>
                <div class="formContent" id="fake-legend">
                    <div class="radioGrp">
                        <label>
                            <input type="radio" name="sampleRadio6" value="" checked="">售票</label>
                        <label>
                            <input type="radio" name="sampleRadio6" value="">免費索票</label>
                        <label>
                            <input type="radio" name="sampleRadio6" value="">自由入場</label>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="formGrp">
        <div class="formTitle">第一層title<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></div>
        <div class="formContent">
            <div class="formGrp">
                <div class="formTitle">第二層title<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></div>
                <div class="formContent">
                    <div class="formGrp">
                        <div class="formTitle">第三層title</div>
                        <div class="formContent formInline ">
                            <input name="" type="text" value="">
                        </div>
                    </div>
                    <div class="formGrp">
                        <div class="formTitle">第三層title</div>
                        <div class="formContent" id="fake-legend">
                            <div class="radioGrp formInline">
                                <label>
                                    <input type="radio" name="sampleRadio6" value="" checked="">A</label>
                                <label>
                                    <input type="radio" name="sampleRadio6" value="">B</label>
                                <label>
                                    <input type="radio" name="sampleRadio6" value="">C</label>
                            </div>
                        </div>
                    </div>
                    <div class="formGrp">
                        <div class="formTitle">第三層title</div>
                        <div class="formContent" id="fake-legend">
                            <div class="radioGrp formInline">
                                <label>
                                    <input type="checkbox" name="sampleRadio6" value="" checked="">A</label>
                                <label>
                                    <input type="checkbox" name="sampleRadio6" value="">B</label>
                                <label>
                                    <input type="checkbox" name="sampleRadio6" value="">C</label>
                            </div>
                        </div>
                    </div>
                    <div class="formGrp">
                        <label for="" class="formTitle">第三層title</label>
                        <div class="formContent formInline address">
                            <select name="" id="">
                                <option value="">台北市</option>
                                <option value="">新北市</option>
                                <option value="">桃園市</option>
                                <option value="">新竹市</option>
                                <option value="">...</option>
                            </select>
                            <select name="" id="">
                                <option value="">中正區</option>
                                <option value="">大安區</option>
                                <option value="">信義區</option>
                                <option value="">北投區</option>
                                <option value="">...</option>
                            </select>
                            <input name="" type="text" value="">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="formGrp">
        <div class="formTitle"> 備註 </div>
        <div class="formContent">
            <textarea name="" id="" cols="30" rows="10"></textarea>
        </div>
    </div>
    <div class="formGrp">
        <div class="formTitle">驗證碼</div>
        <div class="formContent formInline">
            <img src="images/basic/captcha.gif" alt="" class="captcha">
            <input name="" type="text" value="">
            <button class="btn"><i class="i_reflash_deep"></i>重新整理</button>
            <button class="btn"><i class="i_play_deep"></i>語音播放</button>
        </div>
    </div>
    <div class="formGrp agree">
        <div class="formTitle"></div>
        <div class="formContent formInline">
            <div class="checkGrp">
                <label><input name="checkSample" type="checkbox" value="">我已經詳讀以上表單內容</label>
            </div>
        </div>
    </div>
    <div class="btnGrp formInline">
        <button class="btn btnReset">清除</button>
        <button class="btn btnSubmit">送出</button>
    </div>
</div>

<!-- tabs:start -->

#### **HTML**

```html
<div class="flexForm formGrid">
  <div class="formGrp">
    <div class="formTitle">個人資料<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></div>
    <div class="formContent">
      <div class="formGrp">
        <label for="" class="formTitle">姓名<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></label>
        <div class="formContent">
          <input name="" type="text" value="" />
        </div>
      </div>
      <div class="formGrp" role="group" aria-labelledby="fake-legend">
        <label class="formTitle">性別<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></label>
        <div class="formContent" id="fake-legend">
          <div class="radioGrp formInline">
            <label> <input type="radio" name="sampleRadio5" value="" checked="" />男</label>
            <label> <input type="radio" name="sampleRadio5" value="" />女</label>
          </div>
        </div>
      </div>
      <div class="formGrp">
        <div class="formTitle">出生年月日<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></div>
        <div class="formContent formInline birthday">
          <select name="" id="">
            <option value="">2019</option>
            <option value="">2018</option>
            <option value="">2017</option>
            <option value="">2016</option>
            <option value="">...</option></select
          >年
          <select name="" id="">
            <option value="">01</option>
            <option value="">02</option>
            <option value="">03</option>
            <option value="">04</option>
            <option value="">...</option></select
          >月
          <select name="" id="">
            <option value="">01</option>
            <option value="">02</option>
            <option value="">03</option>
            <option value="">04</option>
            <option value="">...</option></select
          >日
        </div>
      </div>
    </div>
  </div>
  <div class="formGrp">
    <div class="formTitle">聯絡方式</div>
    <div class="formContent">
      <div class="formGrp">
        <label for="selectSample" class="formTitle">國家區域</label>
        <div class="formContent formInline">
          <select id="selectSample" name="">
            <option value="">台灣</option>
            <option value="">日本</option>
            <option value="">美國</option>
            <option value="">澳洲</option>
            <option value="">新加坡</option>
            <option value="">中國大陸</option>
          </select>
        </div>
      </div>
      <div class="formGrp">
        <label for="" class="formTitle">手機號碼</label>
        <div class="formContent formInline ">
          <input name="" type="tel" value="" placeholder="0912345678" />
        </div>
      </div>
      <div class="formGrp">
        <label for="" class="formTitle">電話號碼</label>
        <div class="formContent formInline tel">
          <input name="" type="tel" value="" placeholder="886" />
          <input name="" type="tel" value="" placeholder="12345678" />
        </div>
      </div>
      <div class="formGrp">
        <label for="" class="formTitle">傳真號碼</label>
        <div class="formContent formInline tel">
          <input name="" type="tel" value="" placeholder="886" />
          <input name="" type="tel" value="" placeholder="12345678" />
        </div>
      </div>
      <div class="formGrp">
        <label for="" class="formTitle">聯絡地址</label>
        <div class="formContent formInline address">
          <select name="" id="">
            <option value="">台北市</option>
            <option value="">新北市</option>
            <option value="">桃園市</option>
            <option value="">新竹市</option>
            <option value="">...</option>
          </select>
          <select name="" id="">
            <option value="">中正區</option>
            <option value="">大安區</option>
            <option value="">信義區</option>
            <option value="">北投區</option>
            <option value="">...</option>
          </select>
          <input name="" type="text" value="" />
        </div>
      </div>
      <div class="formGrp">
        <div for="" class="formTitle">寄送地址</div>
        <div class="formContent formInline address">
          <label for="" class="labelHidden">縣市</label>
          <select name="" id="">
            <option value="">台北市</option>
            <option value="">新北市</option>
            <option value="">桃園市</option>
            <option value="">新竹市</option>
            <option value="">...</option>
          </select>
          <label for="" class="labelHidden">行政區域</label>
          <select name="" id="">
            <option value="">中正區</option>
            <option value="">大安區</option>
            <option value="">信義區</option>
            <option value="">北投區</option>
            <option value="">...</option>
          </select>
          <label for="" class="labelHidden">詳細地址</label>
          <input name="" type="text" value="" />
          <div class="checkbox">
            <label><input type="checkbox" />同上聯絡地址</label>
          </div>
        </div>
      </div>
      <div class="formGrp">
        <label for="" class="formTitle">公司網站</label>
        <div class="formContent">
          <input name="" type="text" value="" />
        </div>
      </div>
      <div class="formGrp">
        <label for="" class="formTitle">網站URL</label>
        <div class="formContent formInline">
          <select id="selectSample" name="">
            <option value="">http</option>
            <option value="">https</option>
          </select>
          <input type="text" value="" placeholder="www.hyweb.com.tw" />
        </div>
      </div>
    </div>
  </div>
  <div class="formGrp">
    <div class="formTitle">參加活動</div>
    <div class="formContent">
      <div class="formGrp">
        <div class="formTitle">起始日期</div>
        <div class="formContent">
          <div class="datepick">
            <input name="" type="text" value="" class="calendar" placeholder="開始日期" />
            <i class="i_calendar"></i>
          </div>
          <div class="datepick">
            <input name="" type="text" value="" class="calendar" placeholder="結束日期" />
            <i class="i_calendar"></i>
          </div>
        </div>
      </div>
      <div class="formGrp" role="group" aria-labelledby="fake-legend">
        <label class="formTitle">參加場次</label>
        <div class="formContent" id="fake-legend">
          <div class="checkGrp formInline">
            <label> <input type="checkbox" name="" value="" checked="" />全部</label>
            <label> <input type="checkbox" name="" value="" />展覽</label>
            <label> <input type="checkbox" name="" value="" />表演與節慶</label>
            <label> <input type="checkbox" name="" value="" />演講／講座／研討會</label>
            <label> <input type="checkbox" name="" value="" />綜合</label>
          </div>
        </div>
      </div>
      <div class="formGrp">
        <div class="formTitle">有微動態</div>
        <div class="formContent">
          <div class="radioRrp formInline">
            <label><input name="radioSample" type="radio" value="" /><span>選項一</span></label>
            <label><input name="radioSample" type="radio" value="" /><span>選項二</span></label>
            <label><input name="radioSample" type="radio" value="" /><span>其他</span><input type="text" /></label>
          </div>
        </div>
      </div>
      <div class="formGrp">
        <div class="formTitle">有微動態</div>
        <div class="formContent">
          <div class="checkGrp formInline">
            <label><input name="" type="checkbox" value="" /><span>選項一</span></label>
            <label><input name="" type="checkbox" value="" /><span>選項二</span></label>
            <label><input name="" type="checkbox" value="" /><span>選項三</span></label>
          </div>
        </div>
      </div>
      <div class="formGrp" role="group" aria-labelledby="fake-legend">
        <label class="formTitle">參加場次</label>
        <div class="formContent" id="fake-legend">
          <div class="checkGrp">
            <label> <input type="checkbox" name="" value="" checked="" />全部</label>
            <label> <input type="checkbox" name="" value="" />展覽</label>
            <label> <input type="checkbox" name="" value="" />表演與節慶</label>
            <label> <input type="checkbox" name="" value="" />演講／講座／研討會</label>
            <label> <input type="checkbox" name="" value="" />綜合</label>
          </div>
        </div>
      </div>
      <div class="formGrp" role="group" aria-labelledby="fake-legend">
        <legend class="formTitle">是否售票</legend>
        <div class="formContent" id="fake-legend">
          <div class="radioGrp formInline">
            <label> <input type="radio" name="sampleRadio6" value="" checked="" />售票</label>
            <label> <input type="radio" name="sampleRadio6" value="" />免費索票</label>
            <label> <input type="radio" name="sampleRadio6" value="" />自由入場</label>
          </div>
        </div>
      </div>
      <div class="formGrp" role="group" aria-labelledby="fake-legend">
        <label class="formTitle">是否售票</label>
        <div class="formContent" id="fake-legend">
          <div class="radioGrp">
            <label> <input type="radio" name="sampleRadio6" value="" checked="" />售票</label>
            <label> <input type="radio" name="sampleRadio6" value="" />免費索票</label>
            <label> <input type="radio" name="sampleRadio6" value="" />自由入場</label>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="formGrp">
    <div class="formTitle">第一層title<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></div>
    <div class="formContent">
      <div class="formGrp">
        <div class="formTitle">第二層title<abbr class="necessary" title="為必填(選)欄位,不能為空白。">*</abbr></div>
        <div class="formContent">
          <div class="formGrp">
            <div class="formTitle">第三層title</div>
            <div class="formContent formInline ">
              <input name="" type="text" value="" />
            </div>
          </div>
          <div class="formGrp">
            <div class="formTitle">第三層title</div>
            <div class="formContent" id="fake-legend">
              <div class="radioGrp formInline">
                <label> <input type="radio" name="sampleRadio6" value="" checked="" />A</label>
                <label> <input type="radio" name="sampleRadio6" value="" />B</label>
                <label> <input type="radio" name="sampleRadio6" value="" />C</label>
              </div>
            </div>
          </div>
          <div class="formGrp">
            <div class="formTitle">第三層title</div>
            <div class="formContent" id="fake-legend">
              <div class="radioGrp formInline">
                <label> <input type="checkbox" name="sampleRadio6" value="" checked="" />A</label>
                <label> <input type="checkbox" name="sampleRadio6" value="" />B</label>
                <label> <input type="checkbox" name="sampleRadio6" value="" />C</label>
              </div>
            </div>
          </div>
          <div class="formGrp">
            <label for="" class="formTitle">第三層title</label>
            <div class="formContent formInline address">
              <select name="" id="">
                <option value="">台北市</option>
                <option value="">新北市</option>
                <option value="">桃園市</option>
                <option value="">新竹市</option>
                <option value="">...</option>
              </select>
              <select name="" id="">
                <option value="">中正區</option>
                <option value="">大安區</option>
                <option value="">信義區</option>
                <option value="">北投區</option>
                <option value="">...</option>
              </select>
              <input name="" type="text" value="" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="formGrp">
    <div class="formTitle">備註</div>
    <div class="formContent">
      <textarea name="" id="" cols="30" rows="10"></textarea>
    </div>
  </div>
  <div class="formGrp">
    <div class="formTitle">驗證碼</div>
    <div class="formContent formInline">
      <img src="images/basic/captcha.gif" alt="" class="captcha" />
      <input name="" type="text" value="" />
      <button class="btn"><i class="i_reflash_deep"></i>重新整理</button>
      <button class="btn"><i class="i_play_deep"></i>語音播放</button>
    </div>
  </div>
  <div class="formGrp agree">
    <div class="formTitle"></div>
    <div class="formContent formInline">
      <div class="checkGrp">
        <label><input name="checkSample" type="checkbox" value="" />我已經詳讀以上表單內容</label>
      </div>
    </div>
  </div>
  <div class="btnGrp formInline">
    <button class="btn btnReset">清除</button>
    <button class="btn btnSubmit">送出</button>
  </div>
</div>
```

<!-- tabs:end -->

<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4.0/css/style.css" />
<script>
  function addFile() {
  const addFileName = document.querySelectorAll('.check_file');
  addFileName.forEach((i) => {
    i.addEventListener('change', pushFileName);
  });
  function pushFileName(e) {
    let _fileLen = e.target.files.length;
    let _fileName = '';
    const uploadInput = e.target.parentNode.closest('.uploadGrp').querySelector('.upload_file');
    if (_fileLen > 1) {
      _fileName = `${_fileLen} files selected`;
    } else {
      _fileName = e.target.files[0].name;
    }
    uploadInput.value = _fileName;
  }
}
addFile();
</script>
