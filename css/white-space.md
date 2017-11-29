##### white-space
white-space 属性用于指定如何处理容器中的空白字符，例如：空格( )、换行(\n)、缩进(\t)等。

white-space 出自CSS1，适用于块状元素，具有继承性，支持IE 5.5+、Chrome、FireFox、Safari、Opera等所有主流浏览器，`其默认值为 normal`。
#### 属性值
| 值  | 描述  |
| ------------ | ------------ |
| normal  |  默认。空白字符会被浏览器忽略。  |
| pre  |  空白字符会被浏览器全部保留。其行为方式类似 HTML 中的 `<pre>` 标签。  |
| nowrap |  文本不会换行，文本会在在同一行上继续，直到遇到 `<br>`标签为止。  |
| pre-wrap | CSS 2.1新增保留空白符序列，但是正常地进行换行。 |
| pre-line  |  CSS 2.1新增合并空白符序列，但是保留换行符。 |
| inherit  | IE 不支持规定应该从父元素继承 white-space 属性的值。 |
