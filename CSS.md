# CSS编码规范

1.id和class命名，使用小写单词，'-'连接
```
//不推荐
.demoimage {}
.error_status {}
//推荐
#video-id {}
.ads-sample {}
```

2.避免使用id名，标签名，尽量使用class名

3.缩写属性
```
//不推荐
border-top-style: none;
font-family: palatino, georgia, serif;
font-size: 100%;
line-height: 1.6;
padding-bottom: 2em;
padding-left: 1em;
padding-right: 1em;
padding-top: 0;

//推荐
border-top: 0;
font: 100%/1.6 palatino, georgia, serif;
padding: 0 1em 2em;
```

4.省略0后面的单位，使用十六进制
```
//不推荐
padding-bottom: 0px;
margin: 0em;
color: #FF33AA;
//推荐
padding-bottom: 0;
margin: 0;
color: #f3a;
```

5.每个声明应该用分号结束，每个声明换行。
```
//不推荐
.test {
  display: block; height: 100px
}
//推荐
.test {
  display: block;
  height: 100px;
}
```

6.属性和值（但属性和冒号之间没有空格）的之间始终使用一个空格
```
//不推荐
h3 {
  font-weight:bold;
}

//推荐
h3 {
  font-weight: bold;

```

7.属性选择器或属性值用双引号（””），而不是单引号（”）括起来。URI值（url()）不要使用引号。
```
//不推荐
@import url('//cdn.com/foundation.css');
 
html {
  font-family: 'open sans', arial, sans-serif;
}
 
body:after {
  content: 'pause';
}
//推荐
@import url(//cdn.com/foundation.css);
 
html {
  font-family: "open sans", arial, sans-serif;
}
 
body:after {
  content: "pause";
}
```

8.选择器嵌套 (SCSS)
```
//不推荐
.content {
  display: block;
}
 
.content > .news-article > .title {
  font-size: 1.2em;
}
//推荐
.content {
  display: block;
 
  > .news-article > .title {
    font-size: 1.2em;
  }
}
```
9.嵌套顺序和父级选择器(SCSS)

当使用Sass的嵌套功能的时候，重要的是有一个明确的嵌套顺序，以下内容是一个SCSS块应具有的顺序。

当前选择器的样式属性

父级选择器的伪类选择器 (:first-letter, :hover, :active etc)

伪类元素 (:before and :after)

父级选择器的声明样式 (.selected, .active, .enlarged etc.)

用Sass的上下文媒体查询

子选择器作为最后的部分
```
//推荐
.product-teaser {
  // 1. Style attributes
  display: inline-block;
  padding: 1rem;
  background-color: whitesmoke;
  color: grey;
 
  // 2. Pseudo selectors with parent selector
  &:hover {
    color: black;
  }
 
  // 3. Pseudo elements with parent selector
  &:before {
    content: "";
    display: block;
    border-top: 1px solid grey;
  }
 
  &:after {
    content: "";
    display: block;
    border-top: 1px solid grey;
  }
 
  // 4. State classes with parent selector
  &.active {
    background-color: pink;
    color: red;
 
    // 4.2. Pseuso selector in state class selector
    &:hover {
      color: darkred;
    }
  }
 
  // 5. Contextual media queries
  @media screen and (max-width: 640px) {
    display: block;
    font-size: 2em;
  }
 
  // 6. Sub selectors
  > .content > .title {
    font-size: 1.2em;
 
    // 6.5. Contextual media queries in sub selector
    @media screen and (max-width: 640px) {
      letter-spacing: 0.2em;
      text-transform: uppercase;
    }
  }
}
```


