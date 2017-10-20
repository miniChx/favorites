### 刷新页面

- window.location.reload()
- window.history.go(0)
- document.execCommand(''Refresh'') <br/>
这三个方法是最快速的。其他的都有明显的浏览器滚动条的出现。


> Javascript刷新页面的几种方法：

- history.go(0)
- location.reload()
- location=location
- location.assign(location)
- document.execCommand('Refresh')
- window.navigate(location)
- location.replace(location)
- document.URL=location.href

>  Javascript刷新页面的几种方法：

1. `history.go(0)` <br/>
除非有<%..%>等需在服务端解释才能生成的页面代码,否则直接读取缓存中的数据不刷新

1. `location.reload()` <br/>
要重新连服务器以读得新的页面(虽然页面是一样的)刷新

1. `location=location` <br/>
要在javascript中导航，不是调用window对象的某个方法，而是设置它的location.href属性，location属性是每个浏览器都支持的。比如：
`<span onclick="javascript:window.location.href='#top'">top</span>`执行后有后退、前进

1. `location.assign(location)` <br/>
加载 URL 指定的新的 HTML 文档。 就相当于一个链接，跳转到指定的url，当前页面会转为新页面内容，可以点击后退返回上一个页面。

1. ` document.execCommand('Refresh') ` <br/>

1. `window.navigate(location)` <br/>
MSDN说的window.navigate(sURL)方法是针对IE的，不适用于FF，在HTML DOM Window Object中，根本没有列出window.navigate方法。

1. `location.replace(location)` <br/>
执行后无后退、前进通过加载 URL 指定的文档来替换当前文档 ，这个方法是替换当前窗口页面，前后两个页面共用一个窗口，所以是没有后退返回上一页的

1. `document.URL=location.href` <br/>

> 自动刷新页面的方法: javascript自动刷新页面方法详解

1. 页面自动刷新：把如下代码加入<head>区域中
` <meta http-equiv="refresh" content="20"> `
其中20指每隔20秒刷新一次页面

1. 页面自动跳转：把如下代码加入<head>区域中
` <meta http-equiv="refresh" content="20;url=http://www.jbxue.com"> `
其中20指隔20秒后跳转到http://www.jbxue.com页面

1. 页面自动刷新js版
  ```
  <script language="JavaScript">
      function myrefresh()
        {
          window.location.reload();
        }
      setTimeout('myrefresh()',1000); //指定1秒刷新一次
  </script>
  ```

1. JS刷新框架的脚本语句
  ```
  //如何刷新包含该框架的页面用

  <script language=JavaScript>
    parent.location.reload();
  </script>

  //子窗口刷新父窗口

  <script language=JavaScript>
    self.opener.location.reload();
  </script>
  (或<a href="javascript:opener.location.reload()">刷新</a>)

  //如何刷新另一个框架的页面用

  <script language=JavaScript>
    parent.另一FrameID.location.reload();
  </script>
  ```
1. 如果想关闭窗口时刷新或者想开窗时刷新的话，在<body>中调用以下语句即可
  ```
  <body onload="opener.location.reload()"> 开窗时刷新
  <body onUnload="opener.location.reload()"> 关闭时刷新

  <script language="javascript">
    window.opener.document.location.reload()
  </script>
  ```
