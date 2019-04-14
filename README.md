# Menu-gamburger-animate

<h2>HTML</h2>

```html
<div class="btn-menu"><span></span></div>
```

<h2>SASS</h2>

```sass
@media only screen and (max-width: 1200px)
  // burger-menu
  .btn-menu
    position: absolute
    top: 50%
    transform: translateY(-50%)
    right: 20px
    border-radius: 12px
    cursor: pointer
    width: 26px
    height: 36px
    & span::before,
    & span::after,
    & span
      position: absolute
      top: 10px
      margin-top: -1px
      left: 50%
      margin-left: -13px
      width: 26px
      height: 3px
      background-color: #fff
      transition: 0.25s
    &:hover span::before,
    &:hover span::after,
    &:hover span
      background: #fafafa
    & span::before,
    & span::after
      content: ''
      display: block
      transition: 0.25s
    & span::before
      transform: translateY(-2px)
    &_active span
      height: 0
    & span::after
      transform: translateY(5px)
    &_active span:before
      transform: rotate(-45deg)
      transform-origin: center
    &_active span:after
      transform: rotate(45deg)
      transform-origin: center
```

<h2>JS</h2>

```js
$(function(){
    $('.btn-menu').click(function(){
      $(this).toggleClass('btn-menu_active');
      $('.menu').slideToggle();
    });
  });
```
