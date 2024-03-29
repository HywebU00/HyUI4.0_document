# Button 按鈕

?>檔案名稱：sass / element / `btn.scss`

- 按鈕三種寫法：ａ、input、button
- 按鈕三種狀態：default、disabled、readonly
- 按鈕三種樣式：主要、次要、一般
- 按鈕可添加 icon，icon 預設黑色、白色
- 按鈕可添加顏色
- 按鈕可添加大小

<!-- panels:start -->

## 主要、次要、一般按鈕

### button 樣式按鈕

<button type="button" class="btn btnPrimary">主要按鈕</button>
<button type="button" class="btn btnSecondary">次要按鈕</button>
<button type="button" class="btn btnNormal">一般按鈕</button>
<br />

<!--  disabled  -->

<button type="button" class="btn btnPrimary" disabled>主要按鈕</button>
<button type="button" class="btn btnSecondary" disabled>次要按鈕</button>
<button type="button" class="btn btnNormal" disabled>一般按鈕</button>
<br />

<!--  readonly  -->

<button type="button" class="btn btnPrimary" readonly>主要按鈕</button>
<button type="button" class="btn btnSecondary" readonly>次要按鈕</button>
<button type="button" class="btn btnNormal" readonly>一般按鈕</button>

<!-- panels:end -->

<!-- tabs:start -->

#### **HTML**

```html
<!-- button：default、disabled、readonly -->
<div class="btnGrp">
  <div class="btnGrp">
    <button type="button" class="btn btnPrimary">主要按鈕</button>
    <button type="button" class="btn btnSecondary">次要按鈕</button>
    <button type="button" class="btn btnNormal">一般按鈕</button>
    <br />
    <!--  disabled  -->
    <button type="button" class="btn btnPrimary" disabled>主要按鈕</button>
    <button type="button" class="btn btnSecondary" disabled>次要按鈕</button>
    <button type="button" class="btn btnNormal" disabled>一般按鈕</button>
    <br />
    <!--  readonly  -->
    <button type="button" class="btn btnPrimary" readonly>主要按鈕</button>
    <button type="button" class="btn btnSecondary" readonly>次要按鈕</button>
    <button type="button" class="btn btnNormal" readonly>一般按鈕</button>
    <hr />
  </div>
</div>
```

<!-- tabs:end -->
<!-- panels:start -->

<!-- input：default、disabled、readonly icon -->

### input 樣式按鈕

<p>
<input type="button" class="btn btnPrimary" value="主要按鈕" />
<input type="button" class="btn btnSecondary" value="次要按鈕" />
<input type="button" class="btn btnNormal" value="一般按鈕" />
<br />
</p>
<p>
 <!--  disabled  -->
    <input type="button" class="btn btnPrimary" value="主要按鈕" disabled />
    <input type="button" class="btn btnSecondary" value="次要按鈕" disabled />
    <input type="button" class="btn btnNormal" value="一般按鈕" disabled />
    <br />
    </p>
    <!--  readonly  -->
    <input type="button" class="btn btnPrimary" value="主要按鈕" readonly />
    <input type="button" class="btn btnSecondary" value="次要按鈕" readonly />
    <input type="button" class="btn btnNormal" value="一般按鈕" readonly />
<!-- panels:end -->

<!-- tabs:start -->

#### **HTML**

```html
<!-- input：default、disabled、readonly -->
<div class="btnGrp">
  <div class="btnGrp">
    <input type="button" class="btn btnPrimary" value="主要按鈕" />
    <input type="button" class="btn btnSecondary" value="次要按鈕" />
    <input type="button" class="btn btnNormal" value="一般按鈕" />
    <br />
    <!--  disabled  -->
    <input type="button" class="btn btnPrimary" value="主要按鈕" disabled />
    <input type="button" class="btn btnSecondary" value="次要按鈕" disabled />
    <input type="button" class="btn btnNormal" value="一般按鈕" disabled />
    <br />
    <!--  readonly  -->
    <input type="button" class="btn btnPrimary" value="主要按鈕" readonly />
    <input type="button" class="btn btnSecondary" value="次要按鈕" readonly />
    <input type="button" class="btn btnNormal" value="一般按鈕" readonly />
  </div>
</div>
```

<!-- tabs:end -->

<!-- panels:start -->

### a 連結樣式按鈕

<a role="button" href="#" class="btn btnPrimary">主要按鈕</a>
<a role="button" href="#" class="btn btnSecondary">次要按鈕</a>
<a role="button" href="#" class="btn btnNormal">一般按鈕</a>
<br />

<!--  disabled  -->

<a role="button" href="#" class="btn btnPrimary disabled">主要按鈕</a>
<a role="button" href="#" class="btn btnSecondary disabled">次要按鈕</a>
<a role="button" href="#" class="btn btnNormal disabled">一般按鈕</a>
<br />

<!--  readonly  -->

<a role="button" href="#" class="btn btnPrimary readonly">主要按鈕</a>
<a role="button" href="#" class="btn btnSecondary readonly">次要按鈕</a>
<a role="button" href="#" class="btn btnNormal readonly">一般按鈕</a>
<br />

<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
<!-- a連結按鈕：default、disabled、readonly -->
<div class="btnGrp">
  <div class="btnGrp">
    <a role="button" href="#" class="btn btnPrimary">主要按鈕</a>
    <a role="button" href="#" class="btn btnSecondary">次要按鈕</a>
    <a role="button" href="#" class="btn btnNormal">一般按鈕</a>
    <br />
    <!--  disabled  -->
    <a role="button" href="#" class="btn btnPrimary disabled">主要按鈕</a>
    <a role="button" href="#" class="btn btnSecondary disabled">次要按鈕</a>
    <a role="button" href="#" class="btn btnNormal disabled">一般按鈕</a>
    <br />
    <!--  readonly  -->
    <a role="button" href="#" class="btn btnPrimary readonly">主要按鈕</a>
    <a role="button" href="#" class="btn btnSecondary readonly">次要按鈕</a>
    <a role="button" href="#" class="btn btnNormal readonly">一般按鈕</a>
  </div>
</div>
```

<!-- tabs:end -->

## 按鈕顏色

<!-- panels:start -->

<!-- input：default、disabled、readonly icon -->

<button type="button" class="btn btnBlue">按鈕</button>
<button type="button" class="btn btnGreen">按鈕</button>
<button type="button" class="btn btnOrange">按鈕</button>
<button type="button" class="btn btnYellow">按鈕</button>
<button type="button" class="btn btnPurple">按鈕</button>
<button type="button" class="btn btnRed">按鈕</button>

<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
<!-- 按鈕顏色 -->
<div class="btnGrp">
  <div class="btnGrp">
    <button type="button" class="btn btnBlue">按鈕</button>
    <button type="button" class="btn btnGreen">按鈕</button>
    <button type="button" class="btn btnOrange">按鈕</button>
    <button type="button" class="btn btnYellow">按鈕</button>
    <button type="button" class="btn btnPurple">按鈕</button>
    <button type="button" class="btn btnRed">按鈕</button>
  </div>
</div>
```

<!-- tabs:end -->
<!-- panels:start -->

<!-- input：default、disabled、readonly icon -->

## 按鈕大小

<div class="btnGrp" style="text-align: start;">
     <!-- <h3>按鈕大小</h3> -->
    <button class="btn btnXl">特大按鈕</button>
    <button class="btn btnLg">大按鈕</button>
    <button class="btn">按鈕</button>
    <button class="btn btnSm">小按鈕</button>
    <button class="btn btnXs">小小按鈕</button>
    <br />
</div>
<!-- panels:end -->
<!-- tabs:start -->

#### **HTML**

```html
<!-- 按鈕大小 -->
<div class="btnGrp">
  <button class="btn btnXl">特大按鈕</button>
  <button class="btn btnLg">大按鈕</button>
  <button class="btn">按鈕</button>
  <button class="btn btnSm">小按鈕</button>
  <button class="btn btnXs">小小按鈕</button>
</div>
```

<!-- tabs:end -->
<!-- panels:start -->

<!-- 深色 icon -->

## button + 深色 icon

<section>
  <form action="">
    <!-- button + 深色 icon -->
    <div class="btnGrp" style="text-align: left;">
      <button class="btn"><i class="i_apple_dark"></i>IOS</button>
      <button class="btn"><i class="i_arrowLeft_dark"></i>上一頁</button>
      <button class="btn">下一頁<i class="i_arrowRight_dark"></i></button>
      <button class="btn"><i class="i_bookmark_dark"></i>加入書籤</button>
      <button class="btn"><i class="i_chat_dark"></i>訊息</button>
      <button class="btn"><i class="i_check_dark"></i>確認</button>
      <button class="btn"><i class="i_clock_dark"></i>時間</button>
      <button class="btn"><i class="i_close_dark"></i>關閉</button>
      <button class="btn"><i class="i_edit_dark"></i>編輯</button>
      <button class="btn"><i class="i_facebook_dark"></i>facebook</button>
      <button class="btn"><i class="i_grid_dark"></i>清單</button>
      <button class="btn"><i class="i_heart_dark"></i>加入最愛</button>
      <button class="btn"><i class="i_home_dark"></i>回首頁</button>
      <button class="btn"><i class="i_info_dark"></i>說明</button>
      <button class="btn"><i class="i_link_dark"></i>連結</button>
      <button class="btn"><i class="i_linkedin_dark"></i>linkedin</button>
      <button class="btn"><i class="i_lock_dark"></i>鎖定</button>
      <button class="btn"><i class="i_mail_dark"></i>Mail</button>
      <button class="btn"><i class="i_rss_dark"></i>RSS</button>
      <button class="btn"><i class="i_setting_dark"></i>設定</button>
      <button class="btn"><i class="i_star_dark"></i>評比</button>
      <button class="btn"><i class="i_twitter_dark"></i>twitter</button>
      <button class="btn"><i class="i_video_dark"></i>video</button>
      <button class="btn"><i class="i_vimeo_dark"></i>vimeo</button>
      <button class="btn"><i class="i_youtube_dark"></i>youtube</button>
      <button class="btn"><i class="i_order_dark"></i>下單</button>
      <button class="btn"><i class="i_move_dark"></i>移動</button>
      <button class="btn"><i class="i_reflash_dark"></i>重新整理</button>
      <button class="btn"><i class="i_play_dark"></i>語音播放</button>
      <button class="btn"><i class="i_view_dark"></i>檢視</button>
      <button class="btn"><i class="i_add_dark"></i>增加</button>
      <button class="btn"><i class="i_minus_dark"></i>減少</button>
      <button class="btn"><i class="i_search_dark"></i>查詢</button>
      <button class="btn"><i class="i_photo_dark"></i>圖片</button>
      <button class="btn"><i class="i_man_dark"></i>會員</button>
      <button class="btn"><i class="i_copy_dark"></i>複製</button>
      <button class="btn"><i class="i_calendar_dark"></i>日期</button>
    </div>
  </form>
</section>

<!-- panels:end -->

<!-- tabs:start -->

#### **HTML**

```html
<!-- button + 深色 icon -->
<div class="btnGrp">
  <h2>button + 深色 icon</h2>
  <button class="btn"><i class="i_apple_dark"></i>IOS</button>
  <button class="btn"><i class="i_arrowLeft_dark"></i>上一頁</button>
  <button class="btn">下一頁<i class="i_arrowRight_dark"></i></button>
  <button class="btn"><i class="i_bookmark_dark"></i>加入書籤</button>
  <button class="btn"><i class="i_chat_dark"></i>訊息</button>
  <button class="btn"><i class="i_check_dark"></i>確認</button>
  <button class="btn"><i class="i_clock_dark"></i>時間</button>
  <button class="btn"><i class="i_close_dark"></i>關閉</button>
  <button class="btn"><i class="i_edit_dark"></i>編輯</button>
  <button class="btn"><i class="i_facebook_dark"></i>facebook</button>
  <button class="btn"><i class="i_grid_dark"></i>清單</button>
  <button class="btn"><i class="i_heart_dark"></i>加入最愛</button>
  <button class="btn"><i class="i_home_dark"></i>回首頁</button>
  <button class="btn"><i class="i_info_dark"></i>說明</button>
  <button class="btn"><i class="i_link_dark"></i>連結</button>
  <button class="btn"><i class="i_linkedin_dark"></i>linkedin</button>
  <button class="btn"><i class="i_lock_dark"></i>鎖定</button>
  <button class="btn"><i class="i_mail_dark"></i>Mail</button>
  <button class="btn"><i class="i_rss_dark"></i>RSS</button>
  <button class="btn"><i class="i_setting_dark"></i>設定</button>
  <button class="btn"><i class="i_star_dark"></i>評比</button>
  <button class="btn"><i class="i_twitter_dark"></i>twitter</button>
  <button class="btn"><i class="i_video_dark"></i>video</button>
  <button class="btn"><i class="i_vimeo_dark"></i>vimeo</button>
  <button class="btn"><i class="i_youtube_dark"></i>youtube</button>
  <button class="btn"><i class="i_order_dark"></i>下單</button>
  <button class="btn"><i class="i_move_dark"></i>移動</button>
  <button class="btn"><i class="i_reflash_dark"></i>重新整理</button>
  <button class="btn"><i class="i_play_dark"></i>語音播放</button>
  <button class="btn"><i class="i_view_dark"></i>檢視</button>
  <button class="btn"><i class="i_add_dark"></i>增加</button>
  <button class="btn"><i class="i_minus_dark"></i>減少</button>
  <button class="btn"><i class="i_search_dark"></i>查詢</button>
  <button class="btn"><i class="i_photo_dark"></i>圖片</button>
  <button class="btn"><i class="i_man_dark"></i>會員</button>
  <button class="btn"><i class="i_copy_dark"></i>複製</button>
  <button class="btn"><i class="i_calendar_dark"></i>日期</button>
</div>
```

<!-- tabs:end -->

<!-- panels:start -->

<!-- 白色 icon -->

## button + 白色 icon

<section>
  <form action="">
    <div class="btnGrp" style="text-align: left;">
      <button class="btn btnBlue"><i class="i_apple"></i>IOS</button>
      <button class="btn btnBlue"><i class="i_arrowLeft"></i>上一頁</button>
      <button class="btn btnBlue">下一頁<i class="i_arrowRight"></i></button>
      <button class="btn btnBlue"><i class="i_bookmark"></i>加入書籤</button>
      <button class="btn btnBlue"><i class="i_chat"></i>訊息</button>
      <button class="btn btnBlue"><i class="i_check"></i>確認</button>
      <button class="btn btnBlue"><i class="i_clock"></i>時間</button>
      <button class="btn btnBlue"><i class="i_close"></i>關閉</button>
      <button class="btn btnBlue"><i class="i_edit"></i>編輯</button>
      <button class="btn btnBlue"><i class="i_facebook"></i>facebook</button>
      <button class="btn btnBlue"><i class="i_grid"></i>清單</button>
      <button class="btn btnBlue"><i class="i_heart"></i>加入最愛</button>
      <button class="btn btnBlue"><i class="i_home"></i>回首頁</button>
      <button class="btn btnBlue"><i class="i_info"></i>說明</button>
      <button class="btn btnBlue"><i class="i_link"></i>連結</button>
      <button class="btn btnBlue"><i class="i_linkedin"></i>linkedin</button>
      <button class="btn btnBlue"><i class="i_lock"></i>鎖定</button>
      <button class="btn btnBlue"><i class="i_mail"></i>Mail</button>
      <button class="btn btnBlue"><i class="i_rss"></i>RSS</button>
      <button class="btn btnBlue"><i class="i_setting"></i>設定</button>
      <button class="btn btnBlue"><i class="i_star"></i>評比</button>
      <button class="btn btnBlue"><i class="i_twitter"></i>twitter</button>
      <button class="btn btnBlue"><i class="i_video"></i>video</button>
      <button class="btn btnBlue"><i class="i_vimeo"></i>vimeo</button>
      <button class="btn btnBlue"><i class="i_youtube"></i>youtube</button>
      <button class="btn btnBlue"><i class="i_order"></i>下單</button>
      <button class="btn btnBlue"><i class="i_move"></i>移動</button>
      <button class="btn btnBlue"><i class="i_reflash"></i>重新整理</button>
      <button class="btn btnBlue"><i class="i_play"></i>語音播放</button>
      <button class="btn btnBlue"><i class="i_view"></i>檢視</button>
      <button class="btn btnBlue"><i class="i_add"></i>增加</button>
      <button class="btn btnBlue"><i class="i_minus"></i>減少</button>
      <button class="btn btnBlue"><i class="i_search"></i>查詢</button>
      <button class="btn btnBlue"><i class="i_photo"></i>圖片</button>
      <button class="btn btnBlue"><i class="i_man"></i>會員</button>
      <button class="btn btnBlue"><i class="i_copy"></i>複製</button>
      <button class="btn btnBlue"><i class="i_calendar"></i>日期</button>
    </div>
  </form>
</section>
<!-- panels:end -->

<!-- tabs:start -->

#### **HTML**

```html
<!-- button + 白色 icon -->
<div class="btnGrp">
  <button class="btn btnBlue"><i class="i_apple"></i>IOS</button>
  <button class="btn btnBlue"><i class="i_arrowLeft"></i>上一頁</button>
  <button class="btn btnBlue">下一頁<i class="i_arrowRight"></i></button>
  <button class="btn btnBlue"><i class="i_bookmark"></i>加入書籤</button>
  <button class="btn btnBlue"><i class="i_chat"></i>訊息</button>
  <button class="btn btnBlue"><i class="i_check"></i>確認</button>
  <button class="btn btnBlue"><i class="i_clock"></i>時間</button>
  <button class="btn btnBlue"><i class="i_close"></i>關閉</button>
  <button class="btn btnBlue"><i class="i_edit"></i>編輯</button>
  <button class="btn btnBlue"><i class="i_facebook"></i>facebook</button>
  <button class="btn btnBlue"><i class="i_grid"></i>清單</button>
  <button class="btn btnBlue"><i class="i_heart"></i>加入最愛</button>
  <button class="btn btnBlue"><i class="i_home"></i>回首頁</button>
  <button class="btn btnBlue"><i class="i_info"></i>說明</button>
  <button class="btn btnBlue"><i class="i_link"></i>連結</button>
  <button class="btn btnBlue"><i class="i_linkedin"></i>linkedin</button>
  <button class="btn btnBlue"><i class="i_lock"></i>鎖定</button>
  <button class="btn btnBlue"><i class="i_mail"></i>Mail</button>
  <button class="btn btnBlue"><i class="i_rss"></i>RSS</button>
  <button class="btn btnBlue"><i class="i_setting"></i>設定</button>
  <button class="btn btnBlue"><i class="i_star"></i>評比</button>
  <button class="btn btnBlue"><i class="i_twitter"></i>twitter</button>
  <button class="btn btnBlue"><i class="i_video"></i>video</button>
  <button class="btn btnBlue"><i class="i_vimeo"></i>vimeo</button>
  <button class="btn btnBlue"><i class="i_youtube"></i>youtube</button>
  <button class="btn btnBlue"><i class="i_order"></i>下單</button>
  <button class="btn btnBlue"><i class="i_move"></i>移動</button>
  <button class="btn btnBlue"><i class="i_reflash"></i>重新整理</button>
  <button class="btn btnBlue"><i class="i_play"></i>語音播放</button>
  <button class="btn btnBlue"><i class="i_view"></i>檢視</button>
  <button class="btn btnBlue"><i class="i_add"></i>增加</button>
  <button class="btn btnBlue"><i class="i_minus"></i>減少</button>
  <button class="btn btnBlue"><i class="i_search"></i>查詢</button>
  <button class="btn btnBlue"><i class="i_photo"></i>圖片</button>
  <button class="btn btnBlue"><i class="i_man"></i>會員</button>
  <button class="btn btnBlue"><i class="i_copy"></i>複製</button>
  <button class="btn btnBlue"><i class="i_calendar"></i>日期</button>
</div>
```

<!-- tabs:end -->
<link rel="stylesheet" href="https://hywebu00.github.io/HyUI_v4/css/style.css" />
