#### 用 CSS 实现一些简单的效果
- [三角形（各种角度）](#triangle)
- [平行四边形](#parallelogram)
- border-radius

###### [三角形（各种角度）](#triangle)

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle-up.jpg)

```css
.triangle-up {
    width: 0;
    height: 0;
    border-left: 50px solid transparent;
    border-right: 50px solid transparent;
    border-bottom: 100px solid red;
}
```

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle-down.jpg)

```css
.triangle-down {
    width: 0;
    height: 0;
    border-left: 50px solid transparent;
    border-right: 50px solid transparent;
    border-top: 100px solid red;
}
```

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle-left.jpg)

```css
.triangle-left {
    width: 0;
    height: 0;
    border-top: 50px solid transparent;
    border-right: 100px solid red;
    border-bottom: 50px solid transparent;
}
```

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle-right.jpg)

```css
.triangle-right {
    width: 0;
    height: 0;
    border-top: 50px solid transparent;
    border-left: 100px solid red;
    border-bottom: 50px solid transparent;
}
```

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle-topleft.jpg)
<br/>
```css
.triangle-topleft {
    width: 0;
    height: 0;
    border-top: 100px solid red;
    border-right: 100px solid transparent;
}
```

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle-topright.jpg)

```css
.triangle-topright {
    width: 0;
    height: 0;
    border-top: 100px solid red;
    border-left: 100px solid transparent;
}
```

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle-bottomleft.jpg)

```css
.triangle-bottomleft {
    width: 0;
    height: 0;
    border-bottom: 100px solid red;
    border-right: 100px solid transparent;
}
```

![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/mark/triangle-bottomright.jpg)

```css
.triangle-bottomright {
    width: 0;
    height: 0;
    border-bottom: 100px solid red;
    border-left: 100px solid transparent;
}
```



###### [平行四边形](#parallelogram)
