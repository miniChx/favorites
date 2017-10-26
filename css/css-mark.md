#### 用 CSS 实现一些简单的效果
<<<<<<< HEAD
- [三角形](#三角形 "三角形")
- [平行四边形](#平行四边形 "平行四边形")
- [利用border-radius属性绘制一些形状](#border-radius)

> #### 三角形

*利用border绘制三角形*

###### 带边框的三角形
![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle_border_up.jpg)
###### html
```HTML
<!-- 向上的三角形 -->
<div class="triangle_border_up">
  <span></span>
</div>
```
###### css
=======
- [三角形（各种角度）](#triangle)
- [平行四边形](#parallelogram "平行四边形")
- border-radius

###### [三角形（各种角度）](#triangle)

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle-up.jpg)

>>>>>>> a3ec790154b0d5ae77b142e6b6958b274d6c5d8d
```css
/*向上*/
.triangle_border_up{
  width:0;
  height:0;
  border-width:0 30px 30px;
  border-style:solid;
  border-color:transparent transparent #333;/*透明 透明 灰*/
  margin:40px auto;
  position:relative;
}
.triangle_border_up span{
  display:block;
  width:0;
  height:0;
  border-width:0 28px 28px;
  border-style:solid;
  border-color:transparent transparent #fc0;/*透明 透明 黄*/
  position:absolute;
  top:0px;
  left:0px;
}
```

###### 各种角度的三角形
![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle-up.jpg)
![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle-down.jpg)
![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle-left.jpg)
![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle-right.jpg)
```css
.triangle-up {
  width: 0;
  height: 0;
  border-left: 50px solid transparent;
  border-right: 50px solid transparent;
  border-bottom: 100px solid red;
}

.triangle-down {
  width: 0;
  height: 0;
  border-left: 50px solid transparent;
  border-right: 50px solid transparent;
  border-top: 100px solid red;
}

.triangle-left {
  width: 0;
  height: 0;
  border-top: 50px solid transparent;
  border-right: 100px solid red;
  border-bottom: 50px solid transparent;
}

.triangle-right {
  width: 0;
  height: 0;
  border-top: 50px solid transparent;
  border-left: 100px solid red;
  border-bottom: 50px solid transparent;
}
```
![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle.jpg)
![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle-topleft.jpg)
![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle-bottomright.jpg)

```css
.triangle {
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 50px;
  border-color: red transparent transparent transparent;
}

.triangle-top-left {
  width: 0;
  height: 0;
  border-top: 100px solid red;
  border-right: 100px solid transparent;
}

.triangle-bottom-right {
  width: 0;
  height: 0;
  border-bottom: 100px solid red;
  border-left: 100px solid transparent;
}
```

> #### 平行四边形

*利用transform绘制平行四边形*

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/parallelogram.jpg)

###### html
```HTML
<div class="city">
  <span>上海</span>
</div>
```
###### css
```css
.city {
  display: inline-block;
  padding: 5px 20px;
  border: 1px solid #44a5fc;
  color: #333;
  transform: skew(-20deg);
}

.city span {
  transform: skew(20deg);
  display: block;
}
```

> #### border-radius

*利用border-radius属性绘制一些形状*

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/semi-circle.jpg)

```css
.circle{
  width:100px;
  height:100px;
  background-color:#cb18f8;
  border-radius:50px;
}
```

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/border-radius1.jpg)

```css
.roundedCorner {
  width:100px;
  height:100px;
  background-color:#f90;
  border-radius:10px 50px;
}
```

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/border-radius2.jpg)

```css
.roundedCorner {
  width:100px;
  height:100px;
  background-color:#f90;
  border-radius:10px 100px;
}
```
