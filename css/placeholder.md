#### css3中设置placeholder的样式
*placeholder属性是css3中新增加的属性，IE9和Opera12以下版本的CSS选择器均不支持占位文本。那么怎样设置它的默认字体颜色呢？*

```css
  input::-webkit-input-placeholder {
    color: #aab2bd;     /* 颜色  */
    font-size: 12px;    /* 字体大小 */
    text-align: right;  /* 位置  */
  }
```

因为每个浏览器的CSS选择器都有所差异，所以需要针对每个浏览器做单独的设定(可以在冒号前面写input和textarea)。
```css
  /* WebKit browsers */
  input::-webkit-input-placeholder,
  textarea::-webkit-input-placeholder {
    color: #666;
  }
  
  /* Mozilla Firefox 4 to 18 */
  input:-moz-placeholder,
  textarea:-moz-placeholder {
    color:#666;
  }
  
  /* Mozilla Firefox 19+ */
  input::-moz-placeholder,
  textarea::-moz-placeholder {
    color:#666;
  }
  
  /* Internet Explorer 10+ */
  input:-ms-input-placeholder,
  textarea:-ms-input-placeholder {
    color:#666;
  }
```

还可以写成下面这样：
```css
  /* WebKit browsers */
  ::-webkit-input-placeholder {
    color:#999;
  }
  
  /* Mozilla Firefox 4 to 18 */
  :-moz-placeholder {
    color:#999;
  }
  
  /* Mozilla Firefox 19+ */
  ::-moz-placeholder {
    color:#999;
  }
  
  /* Internet Explorer 10+ */
  :-ms-input-placeholder {
    color:#999;
  }
```
