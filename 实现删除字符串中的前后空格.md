#### javascript中使用正则表达式实现删除字符串中的前后空格

###### *我们经常会碰到 要删除用户输入的字符中的空格的问题，此篇记录了javascript中使用正则表达式实现删除字符串中的空格方法*


```javascript
<script type="text/javascript"> 
	
	// 删除字符串两侧的空白字符 
	function trim(str){ 
		return str.replace(/(^\s*)|(\s*$)/g,''); 
	} 

	// 删除字符串左侧的空白字符 
	function lTrim(str){ 
		return str.replace(/(^\s*)/g,''); 
	} 

	// 删除字符串右侧的空白字符
	function rTrim(str){ 
		return str.replace(/(\s*$)/g,''); 
	} 

	// 以下为测试代码,前后各有一个空格 
	var trimTest = " 123456789 "; 

	// 使用前  
	document.write('length: '+trimTest.length+'<br />'); 

	// 使用trim后 
	document.write('trim length: '+trim(trimTest).length+'<br />'); 

	// 使用lTrim后 
	document.write('lTrim length: '+lTrim(trimTest).length+'<br />'); 

	// 使用rTrim后 
	document.write('rTrim length: '+rTrim(trimTest).length+'<br />'); 

</script>
```
