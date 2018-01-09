#### 关于 clear 的小总结

语法：
clear : none | left | right | both

| 取值  | 定义                             |
| ----- | -------------------------------- |
| none  | 默认值。允许两边都可以有浮动对象 |
| left  | 清除前一个 div 的 float：left    |
| right | 清除前一个 div 的 float：right   |
| both  | 清除前一个 div 的浮动属性        |

> 关于 left & right

###### left & right 的使用，是根据前一个 div 设置的 float 属性

* left

  ```
  css:

  <style>
   .box1, .box2 {
     height: 100px;
     float: left; /* 划重点 */
   }

   .box1 {
      width: 100px;
      background: red;
    }

    .box2 {
      clear: left;  /* 划重点 */
      width: 200px;
      background: blue;
    }
  </style>

  html:

  <div class="box1">box1</div>
  <div class="box2">box2</div>
  ```

- right

  ```
  css:

  <style>
   .box1, .box2 {
     height: 100px;
     float: right; /* 划重点 */
   }

   .box1 {
      width: 100px;
      background: red;
    }

    .box2 {
      clear: right;  /* 划重点 */
      width: 200px;
      background: blue;
    }
  </style>

  html:

  <div class="box1">box1</div>
  <div class="box2">box2</div>
  ```
