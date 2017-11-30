# fe-code-specification
frontend code specification

# 一般规范

1.文件/资源命名

使用小写单词，减号分隔，min后缀使用点号
```
//不推荐
MyScript.js
myCamelCaseName.css
i_love_underscores.html
1001-scripts.js
my-file-min.css
//推荐
my-script.js
my-camel-case-name.css
i-love-underscores.html
thousand-and-one-scripts.js
my-file.min.css
```

2.协议

不要指定引入资源所带的具体协议
```
//不推荐
<script src="http://cdn.com/foundation.min.js"></script>
.example {
  background: url(http://static.example.com/images/bg.jpg);
}
//推荐
<script src="//cdn.com/foundation.min.js"></script>
.example {
  background: url(//static.example.com/images/bg.jpg);
}
```

3.文本缩进，一次使用4个空格 

4.js类文件，组件文件，服务文件名使用首字母大写单词命名
```
//不推荐
home-page.js
button.js
user_service.js
//推荐
HomePage.js
Button.js
UserService.js
```













