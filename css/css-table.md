#### css 给table加边框：
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
	<table>
	  <tr><td>内容</td><td>内容</td><td>内容</td><td>内容</td><td>内容</td></tr>
	  <tr><td>内容</td><td>内容</td><td>内容</td><td>内容</td><td>内容</td></tr>
	  <tr><td>内容</td><td>内容</td><td>内容</td><td>内容</td><td>内容</td></tr>
	  <tr><td>内容</td><td>内容</td><td>内容</td><td>内容</td><td>内容</td></tr>
	</table>
```
效果如图：<br/>
![Aaron Swartz](https://raw.githubusercontent.com/miniChx/favorites/master/css/imgs/css-table.jpg)
