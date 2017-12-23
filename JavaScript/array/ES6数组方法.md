### ES6数组方法
以下方法添加到了Array.prototype对象上（isArray除外）

- #### indexOf
类似字符串的indexOf()方法
```javascript
stringObject.indexOf(searchvalue,fromindex)
var data = [2, 5, 7, 3, 5];
console.log(data.indexOf(5, "x")); // 1 ("x"被忽略)
console.log(data.indexOf(5, "3")); // 4 (从3号位开始搜索)
console.log(data.indexOf(4)); // -1 (未找到)
console.log(data.indexOf("5")); // -1 (未找到，因为5 !== "5")
```

- #### lastIndexOf
类似indexOf()方法（顺序相反）

- #### forEach
Array在ES5新增的方法中，参数都是function类型，默认有传参(遍历的数组内容,对应的数组索引,数组本身)
```javascript
	[].forEach(function(value, index, array) {
		// ...
	});
```
forEach方法 遍历数组元素
```javascript
var colors = ['red', 'green', 'blue'];
colors.forEach(function(color) {
	console.log(color);
});
```
forEach除了接受一个必须的回调函数参数，还可以接受一个可选的上下文参数（改变回调函数里面的this指向）（第2个参数）如果这第2个可选参数不指定，则使用全局对象代替（在浏览器是为window），严格模式下甚至是undefined

###### array.forEach(callback,[ thisObject])

- #### map
映射（一一对应）。[].map();基本用法跟forEach方法类似：
`array.map(callback,[ thisObject]);`
但是callback需要有return值（如果没有，就像会返回undefined）
```javascript
var a1 = ['a', 'b', 'c'];
var a2 = a1.map(function(item) {
	return item.toUpperCase()
});
console.log(a2); // logs A,B,C
```
- #### filter
过滤筛选（callback在这里担任的是过滤器的角色，当元素符合条件，过滤器就返回true，而filter则会返回所有符合过滤条件的元素）。
`array.filter(callback,[ thisObject]);`
指数组filter后，返回过滤后的新数组。用法跟map相似
```javascript
var a1 = ['a', 10, 'b', 20, 'c', 30];
var a2 = a1.filter(function(item) {
	return typeof item == 'number';
});
console.log(a2); // logs 10,20,30
```
- #### every(且)
every(callback[, thisObject])当数组中每一个元素在callback上被返回true时就返回true。
```javascript
function isNumber(value){ 
    return typeof value == 'number';
}
var a1 = [1, 2, 3];
console.log(a1.every(isNumber)); // logs true
var a2 = [1, '2', 3];
console.log(a2.every(isNumber)); // logs false
```

- #### some(或)
some(callback[, thisObject]) 只要数组中有一项在callback上被返回true，就返回true。
```javascript
function isNumber(value){ 
return typeof value == 'number';
}
var a1 = [1, 2, 3];
console.log(a1.some(isNumber)); // logs true
var a2 = [1, '2', 3];
console.log(a2.some(isNumber)); // logs true
var a3 = ['1', '2', '3'];
console.log(a3.some(isNumber)); // logs false
```
- #### reduce(从左到右累加)
对数组中的所有元素调用指定的回调函数。该回调函数的返回值为累积结果，并且此返回值在下一次调用该回调函数时作为参数提供。
```javascript
var a = [10, 20, 30];
var total = a.reduce(function(first, second) {
	return first + second;
}, 0);
console.log(total) // Prints 60
```

- #### reduceRight(从右到左累加)
reduce的作用完全相同，唯一的不同是，reduceRight是从右至左遍历数组的元素。

- #### Array构造器上的isArray
Array.isArray直接写在了Array构造器上，而不是prototype对象上。Array.isArray会根据参数的[[Class]]内部属性是否是”Array”返回true或false.
```javascript
Array.isArray("NO U")
falseArray.isArray(["NO", "U"])// true
```

- #### Array.prototype.slice.call
真实数组具有slice方法，可以对数组进行浅复制（不影响原数组），返回的依然是数组。类似数组虽然有length属性，可以使用for循环遍历，却不能直接使用slice方法，会报错！但是通过Array.prototype.slice.call则不会报错，本身（类似数组）被从头到尾slice复制了一遍——变成了真实数组！
###### 将类似数组的对象(比如arguments)转换为真实的数组
`Array.prototype.slice.call(arguments)`
