#### CSS实现单行、多行文本溢出显示省略号（...）
> 单行文本 溢出显示省略号

```css
overflow: hidden;
text-overflow:ellipsis;
white-space: nowrap;
```
效果如图：<br/>
![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/text-overflow1.jpg)
<br/>

>多行文本 溢出显示省略号

```css
display: -webkit-box;
-webkit-box-orient: vertical;
-webkit-line-clamp: 3;
overflow: hidden;
```
效果如图：<br/>
![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/text-overflow2.jpg)
<br/>
适用范围：
因使用了WebKit的CSS扩展属性，该方法适用于WebKit浏览器及移动端；

###### 注：
###### -webkit-line-clamp用来限制在一个块元素显示的文本的行数。 为了实现该效果，它需要组合其他的WebKit属性。常见结合属性：
###### 1. display: -webkit-box; 必须结合的属性 ，将对象作为弹性伸缩盒子模型显示 。
###### 2. -webkit-box-orient 必须结合的属性 ，设置或检索伸缩盒对象的子元素的排列方式 。

> 蒙版效果

```css
p{
 position: relative;
 line-height: 20px;
 max-height:40px;
 overflow: hidden;
}
p::after{
 content: "...";
 position: absolute;
 bottom: 0;
 right: 0;
 padding-left: 40px;
 background: -webkit-linear-gradient(left, transparent, #fff 55%);
 background: -o-linear-gradient(right, transparent, #fff 55%);
 background: -moz-linear-gradient(right, transparent, #fff 55%);
 background: linear-gradient(to right, transparent, #fff 55%);
}
```
效果如图：<br/>
![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/text-overflow3.jpg)
<br/>
适用范围：
该方法适用范围广，但文字未超出行的情况下也会出现省略号,可结合js优化该方法。

注：<br/>
将height设置为line-height的整数倍，防止超出的文字露出。<br/>
给p::after添加渐变背景可避免文字只显示一半。<br/>
由于ie6-7不显示content内容，所以要添加标签兼容ie6-7（如：<span>…<span/>）；兼容ie8需要将::after替换成:after。


#### CSS控制文字换行、裁剪

<font color=red size=3>文字溢出显示省略标记（...）</font>

```css
text-overflow: ellipsis;
overflow: hidden;
white-space: nowrap;
```
<font color=red size=3>文字换行</font>

```css
/* 以单词作为换行依据 */
word-wrap: break-word;
word-break: normal;

/* 以字母作为换行依据 */
word-break: break-all;
```

<font color=red size=3>文字强制不换行</font>

```css
white-space: nowrap;
```

#### 概念：关于换行、裁剪的一些CSS属性
```css
word-wrap: normal  |  break-word
```

| 属性  | 描述  |
| :------------ | :------------ |
| normal  | 正常换行，内容可以撑破容器，例如长单词或者长数字的情况  |
| break-word  | 以单词作为换行依据，如果需要，单词内部允许断行  |

```css
word-break: normal  |  break-all  |  keep-all
```

| 属性  | 描述  |
| :------------ | :------------ |
| normal  | 正常换行，内容可以撑破容器，例如长单词或者长数字的情况  |
| break-all  | 以字母作为换行依据  |
| keep-all  | 中英文下和normal相同  |

 ```css
white-space: normal | pre | nowrap | pre-line | pre-wrap | inherit
```

| 属性  | 描述  |
| :------------ | :------------ |
| normal  | 默认值，空白会被浏览器忽略  |
| pre | 空白会被浏览器保留，其行为方式类似 HTML 中的 `<pre>` 标签  |
| nowrap | 文本不会换行，文本会在在同一行上，直到遇到 `<br />` 标签为止  |
| pre-wrap | 保留空白符序列，但是正常地进行换行(IE7-不支持) |
| pre-line | 合并空白符序列，但保留换行符(IE7-不支持)  |
| inherit | 规定应该从父元素继承 white-space 属性的值(IE不支持)  |
