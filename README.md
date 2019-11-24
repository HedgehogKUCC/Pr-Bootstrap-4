# 最終作業 - 甜點電商

[gh-pages](https://hedgehogkucc.github.io/Pr-Bootstrap-4/)

## 修改 _variables.scss

`!default` 記得要拿掉不然會被後面覆蓋過去，因為權重很輕 !!!

## 使用 block 傳遞 var

[jade-pass-variables](https://stackoverflow.com/questions/12646451/how-to-pass-variables-between-jade-templates)

## Broken-images on gh-pages

[Broken-images](https://github.community/t5/GitHub-Pages/Broken-images/td-p/13674)

## header 區塊 - 透明玻璃效果

`no-gutters` : 消除 `row` 設定的 `margin-left: -15px` & `margin-right: -15px`

利用 `z-index` 來決定元素堆疊順序 [連結1](https://www.webdesigns.com.tw/css-_z-index.asp) [連結2](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index)

    注意 :
          z-index 只能在有設定位（position）的元素上才會奏效 !!!
          可設定為 position: static、absolute、relative、fixed

`rectangle-image-wrap` 設定 `z-index: 2;`

`rectangle-text` 沒有設定會是 `z-index: auto;`

`four-sides` 設定 `z-index: -1;` 、 `rectangle-over` 設定 `background-color` 和 `transition`

`rectangle-image` 設定 `z-index: -2;` [CSS濾鏡效果 - filter](http://blog.shihshih.com/css-filter/)

```html
<div class="container px-0 px-md-3">
  <header class="header">
    <div style="background-image: url(...)" class="header-main-image bg-cover"></div>
    <h1 class="text-hide">...</h1>
    <div class="row no-gutters justify-content-center rectangle-section">
      <div class="col-md-10">
        <div class="row no-gutters">
          <a href="#" class="col-4 rectangle-image-wrap">
            <span class="rectangle-text">本日精選</span>
            <div class="four-sides rectangle-over"></div>
            <div style="background-image: url(...)" class="rectangle-image bg-cover"></div>
          </a>
          <a href="#" class="col-4 rectangle-image-wrap">
            ...
          </a>
          <a href="#" class="col-4 rectangle-image-wrap">
            ...
          </a>
        </div>
      </div>
    </div>
  </header>
</div
```