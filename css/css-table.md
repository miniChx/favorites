#### css给table加边框：
css：
```css
<style>
	table,table tr th, table tr td {
		border:1px solid #0094ff;
	}
	table {
		width: 200px;
		min-height: 25px;
		line-height: 25px;
		text-align: center;
		border-collapse: collapse;
		padding:2px;
	}
</style>
```
html：
```html
	<table >
		<tr><td>内容</td><td>内容</td><td>内容</td><td>内容</td><td>内容</td></tr>
		<tr><td>内容</td><td>内容</td><td>内容</td><td>内容</td><td>内容</td></tr>
		<tr><td>内容</td><td>内容</td><td>内容</td><td>内容</td><td>内容</td></tr>
		<tr><td>内容</td><td>内容</td><td>内容</td><td>内容</td><td>内容</td></tr>
	</table>
```
效果如图：<br/>
![Alt text](http://images2015.cnblogs.com/blog/995687/201612/995687-20161202151555959-624405021.png)
