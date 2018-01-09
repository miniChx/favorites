### CSS3制作各种形状图像
- [三角形](#三角形 "三角形")
- [平行四边形](#平行四边形 "平行四边形")
- [利用border-radius属性绘制一些形状](#border-radius)
- [多边形](#多边形)
- [其他](#其他)

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

> #### 多边形

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/star.jpg)

```css
#star {
    width: 0;
    height: 0;
    margin: 50px 0;
    color: #fc2e5a;
    position: relative;
    display: block;
    border-right: 100px solid transparent;
    border-bottom: 70px solid #fc2e5a;
    border-left: 100px solid transparent;
    -moz-transform: rotate(35deg);
    -webkit-transform: rotate(35deg);
    -ms-transform: rotate(35deg);
    -o-transform: rotate(35deg);
}

#star:before {
    height: 0;
    width: 0;
    position: absolute;
    display: block;
    top: -45px;
    left: -65px;
    border-bottom: 80px solid #fc2e5a;
    border-left: 30px solid transparent;
    border-right: 30px solid transparent;
    content: '';
    -webkit-transform: rotate(-35deg);
    -moz-transform: rotate(-35deg);
    -ms-transform: rotate(-35deg);
    -o-transform: rotate(-35deg);
}

#star:after {
    content: '';
    width: 0;
    height: 0;
    position: absolute;
    display: block;
    top: 3px;
    left: -105px;
    color: #fc2e5a;
    border-right: 100px solid transparent;
    border-bottom: 70px solid #fc2e5a;
    border-left: 100px solid transparent;
    -webkit-transform: rotate(-70deg);
    -moz-transform: rotate(-70deg);
    -ms-transform: rotate(-70deg);
    -o-transform: rotate(-70deg);
}
```

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/star_six_points.jpg)

```css
#star_six_points {
  width: 0;
  height: 0;
  display: block;
  position: absolute;
  border-left: 60px solid transparent;
  border-right: 60px solid transparent;
  border-bottom: 100px solid #de34f7;
  margin: 150px;
}

#star_six_points:after {
  content: "";
  width: 0;
  height: 0;
  position: absolute;
  border-left: 60px solid transparent;
  border-right: 60px solid transparent;
  border-top: 100px solid #de34f7;
  margin: 33px 0 0 -60px;
}
```

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/hexagon.jpg)

```css
#hexagon {
  width: 100px;
  height: 55px;
  background: #fc5e5e;
  position: relative;
  margin: 10px auto;
}

#hexagon:before {
  content: "";
  width: 0;
  height: 0;
  position: absolute;
  top: -25px;
  left: 0;
  border-left: 50px solid transparent;
  border-right: 50px solid transparent;
  border-bottom: 25px solid #fc5e5e;
}

#hexagon:after {
  content: "";
  width: 0;
  height: 0;
  position: absolute;
  bottom: -25px;
  left: 0;
  border-left: 50px solid transparent;
  border-right: 50px solid transparent;
  border-top: 25px solid #fc5e5e;
}
```

> #### 其他

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/heart.jpg)

```css
#heart {
  position: relative;
}

#heart:before,#heart:after {
  content: "";
  width: 70px;
  height: 115px;
  position: absolute;
  background: red;
  left: 70px;
  top: 0;
  -webkit-border-radius: 50px 50px 0 0;
  -moz-border-radius: 50px 50px 0 0;
  border-radius: 50px 50px 0 0;
  -webkit-transform: rotate(-45deg);
  -moz-transform: rotate(-45deg);
  -ms-transform: rotate(-45deg);
  -o-transform: rotate(-45deg);
  transform: rotate(-45deg);
  -webkit-transform-origin: 0 100%;
  -moz-transform-origin: 0 100%;
  -ms-transform-origin: 0 100%;
  -o-transform-origin: 0 100%;
  transform-origin: 0 100%;
}

#heart:after {
  left: 0;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
  transform: rotate(45deg);
  -webkit-transform-origin: 100% 100%;
  -moz-transform-origin: 100% 100%;
  -ms-transform-origin: 100% 100%;
  -o-transform-origin: 100% 100%;
  transform-origin: 100% 100%;
}
```

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/egg.jpg)

```css
#egg {
  width: 136px;
  height: 190px;
  background: #ffc000;
  display: block;
  -webkit-border-radius: 63px 63px 63px 63px / 108px 108px 72px 72px;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}
```

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/infinity.jpg)

```css
#infinity {
  width: 220px;
  height: 100px;
  position: relative;
}

#infinity:before,#infinity:after {
  content: "";
  width: 60px;
  height: 60px;
  position: absolute;
  top: 0;
  left: 0;
  border: 20px solid #06c999;
  -moz-border-radius: 50px 50px 0;
  border-radius: 50px 50px 0 50px;
  -webkit-transform: rotate(-45deg);
  -moz-transform: rotate(-45deg);
  -ms-transform: rotate(-45deg);
  -o-transform: rotate(-45deg);
  transform: rotate(-45deg);
}

#infinity:after {
  left: auto;
  right: 0;
  -moz-border-radius: 50px 50px 50px 0;
  border-radius: 50px 50px 50px 0;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
  transform: rotate(45deg);
}
```

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/comment_bubble.jpg)

```css
#comment_bubble {
  width: 140px;
  height: 100px;
  background: #088cb7;
  position: relative;
  -moz-border-radius: 12px;
  -webkit-border-radius: 12px;
  border-radius: 12px;
}

#comment_bubble:before {
  content: "";
  width: 0;
  height: 0;
  right: 100%;
  top: 38px;
  position: absolute;
  border-top: 13px solid transparent;
  border-right: 26px solid #088cb7;
  border-bottom: 13px solid transparent;
}
```
