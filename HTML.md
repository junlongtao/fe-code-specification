# HTML编码规范

1.引入js放置最后，添加async
```
//不推荐
<html>
  <head>
    <link rel="stylesheet" href="main.css">
    <script src="main.js" async></script>
  </head>
  <body>
    <!-- body goes here -->
  </body>
</html>
//推荐
<html>
  <head>
    <link rel="stylesheet" href="main.css">
  </head>
  <body>
    <!-- body goes here -->
 
    <script src="main.js" async></script>
  </body>
</html>
```

2.标签语义化，如，用 heading 元素来定义头部标题，p 元素来定义文字段落，用 a 元素来定义链接锚点。

3.不使用行内样式（```<style>.no-good{}</style>```), 不使用style属性（```<hr style="border-top: 5px solid black">```），不使用行内脚本（```<script>alert('no good')</script>```）
，不使用表象元素（```i.e. <b>, <u>, <center>, <font>, <b>```）， 不使用表象 class 名（```i.e. red, left, center```）

4.HTML只关注内容，不用于展现设计
```
//不推荐
<span class="text-box">
  <span class="square"></span>
  See the square next to me?
</span>
.text-box > .square {
  display: inline-block;
  width: 1rem;
  height: 1rem;
  background-color: red;
}

//推荐
<span class="text-box">
  See the square next to me?
</span>
.text-box:before {
  content: "";
  display: inline-block;
  width: 1rem;
  height: 1rem;
  background-color: red;
}
```

5.省略type属性
```
//不推荐
<link rel="stylesheet" href="main.css" type="text/css">
<script src="main.js" type="text/javascript"></script>
//推荐
<link rel="stylesheet" href="main.css">
<script src="main.js"></script>
```

6.块状元素，列表元素，表格元素后，加空白行进行换行，并对子孙元素缩进
```
//推荐
<blockquote>
    <p><em>Space</em>, the final frontier.</p>
</blockquote>

<ul>
    <li>Moe</li>
    <li>Larry</li>
    <li>Curly</li>
</ul>

<table>
    <thead>
    <tr>
        <th scope="col">Income</th>
        <th scope="col">Taxes</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>$ 5.00</td>
        <td>$ 4.50</td>
    </tr>
    </tbody>
</table>
```

7.使用双引号
```
//不推荐
<div class='news-article'></div>
//推荐
<div class="news-article"></div>

```
