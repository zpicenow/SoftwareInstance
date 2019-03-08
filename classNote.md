# 微信小程序开发之路  
----  
# 第一部分——HTML  
---  

+ HTML是超文本标记语言的缩写,它不是一种编程语言，它是一种标记语言  
+ 浏览器是解释和执行HTML的工具，标签用来描述网页，因此网页不会显示标签  

#### \<meta>标签  
+ 描述文档类型和字符编码  ,比如其中的charset，通常设置为UTF-8，防止浏览器载入时乱码
+ 提供网页检索的依据  ，比如name属性中定义的关键词就是搜索引擎分类检索的依据

#### html标签分类  

+ 块级标签：显示为块状，前后隔一行  
+ 行级标签：显示为行  

#### 常用标签  

+ 可以用\<title>name\</title>定义页面名称
+ 标题标签：\<h1>标题\</h1>,提供h1到h6的标题风格  
+ 段落标签：\<p>段落\</p>,前后换行，为一个自然段  
+ 分割线标签： \<hr/>，提供一行分割线，不成对  
+ 有序列表： 列表元素带数字序号
```html
<ol>
<li>coffee</li>
<li>tea</li>
<li>water</li>

</ol>   

```  
+ 无序列表： 列表元素用原点分布  
```html
<ul>
<li>coffe</li>
<li>tea</li>
<li>water</li>
</ul>
//简单嵌套


<h4>一个嵌套列表：</h4>
<ul>
  <li>咖啡</li>
  <li>  茶
    <ul>
    <li>红茶</li>
    <li>绿茶
      <ul>
      <li>中国茶</li>
      <li>非洲茶</li>
      </ul>
    </li>
    </ul>
  </li>
  <li>牛奶</li>
</ul>

```
+ 定义描述标签： 形式为给出词语及解释  
```html
<dl>
<dt>title</dt>
<dd>define</dd>


</dl>

``` 
+ 表格标签：  其中border属性表示边框尺寸，tr声明行，td声明列，有几对就是有几行，每行里面有几列
```html
<table border="1">
<tr>
<td colspan="2">1</td>
<td>2</td>
<td>3</td>
</tr>

</table>


```  
colspan 是跨列数；rowspan是跨行数;th标签是表头

+ 表单标签：  form为用户创建输入表单，
```html
<form >
    name:
    <input type="text" name="inch">
    <br/>
    sex:
    <input type="checkbox" name="insex">
</form>
```
input类型有很多种，包括submit和reset，分别是提交和重置键，对于动态链接  
```html
<form action="www.xxx" method="get/post"></form>
```  
其中get方法将数据写在地址栏上，获取方便但不安全  
post方法将数据放到内存中，更安全  
value属性是显示在页面的内容  
输入框的size是显示的长度，maxlength是允许输入的最大长度  
radio作为单选框，两个name要相同，而checkbox是复选框，各名字不能相同  

+ 文件域，form的type是file，结合submit上传  

+ 下拉菜单：   
```html
<select name="xx" style="width: 30%">
    <option value="0">No1</option>
    <option value="0">No2</option>
    <option value="0">No3</option>
    <option value="0">&copy</option>
</select>
```


+ 图像标签与属性  ：图片地址有相对地址和绝对地址两类，相对地址主要有相对文件路径等，
绝对地址比如超链接等，对于不同的图片类型写入的格式是一样的，因为本身带有后缀名，浏览器也能够呈现出该有的状态

在body中也可以设定background属性，指定网页的背景图，图片过小会重复  
通过align属性可以设定布局，相对于文字的位置等，默认值是bottom  ，设置为left/right属性可以指定浮动至段落的左侧或右侧  
指定的alt属性，如果图片正常加载，鼠标悬浮于图片上时会显示alt文本，如果图片无法加载，会替换为alt文本
```html
<img src="图片地址" alt="图像的代替文本"/>
<img src="/xx/xx/xx.jpg" />
<img src="http://www.xxxxxx/xxx.gif"/>
<img src="xxx" align="布局值bottom/middle/top"/>

```
*相对地址不安全，容易被攻击*  

+ 强调标签：\<span>text\</span>  
+ 换行标签： \<br/>此标签没有空行，两个p标签之间会空行  

+ 范围标签：div标签用来划分块

+ 链接标签 ：   a标签，也叫做anchor锚点元素，href属性是目的的超链接，通过对href值的设定完成不同的跳转需要  
```html
<a href="http://www.baidu.com">baidu</a>

//图片超链接
<a href="xxx">
<img src="/xxx/xxx"/>
</a>

//连接到页面其他位置
<a href="#名字">to'name'</a>
<p>无关段落</p>
<h3><a name="名字">我是标题3，也是要跳转的地方</a> </h3>
//或者使用id属性，作用和name相同
<a href="#name">to 'name'</a>
<p>wuguan </p>

<p><a id="name">to here</a> </p>

//在新页面打开链接，只需将target设置为_blank
<a href="xxxxxx" target="_blank">新页面打开</a>

```
#### 实际开发中常用的四种块状结构  

+ div-ul(ol)-li: 用于分类导航或菜单  
+ div-dl-dt-dd: 用于图文混合编辑  
+ table-tr-td: 用于行列表  
+ form-table-tr-td: 用于布局表单    
   
**万维网制定规范标准**
+ 标签名属性名必须小写  
+ 标签必须关闭  
+ 属性值必须用引号  
+ 标签必须正确嵌套
+ 必须添加文档类型声明   


#### 特殊符号  
+ 空格： &nbsp  
+ 大于号： &gt  
+ 小于号：&lt
+ 引号： &quot
+ 版权号： &copy


### 框架  
很多网页顶部有不变的logo，左侧是固定的导航栏，当点击导航栏时只有右侧的区域随之变动，像这种只有部分区域响应变化的布局，就是用框架实现的
#### frameset  
frameset不能和body同用
```html
<frameset columns="25%,50%,*" rows="50%, *">
    <frame src="xxx/xx.html" name="xx"/>
    <frame src="xxx/xxx.html" name="xxx" scrolling="no" noresize="noresize">
</frameset>
```  
第一行是按列划分为占比25,50，和25的三部分，*就是代表余下全部  
最后一行scrolling设置的是不显示滚动条，noresize设置的是图片不拉伸  
下面的代码可以实现上面说的T型布局，   
```html
<frameset rows="20%,*">
    <frame>logo
    <frameset columns="20%,*">
        <frame>左侧导航栏
        <frame name="rightframe">显示区
    </frameset>
</frameset>

<!--然后对于触发链接只要在target指定目的域即可，目的域就是前文命名的frame的name-->
<a href="xxx" target="rightframe"></a>

```
#### iframe  
frameset不能和body同用，这就造成了很多麻烦，因袭引入iframe  
iframe使用非常简单  
```html
<iframe src="引用地址" name="标识" scrolling="no"/>
```  
相对于frameset更好，目前frameset官方已经不建议使用  


### HTML应用CSS  

css是层叠样式表的缩写，从html4开始使用，是为了更好地渲染HTML元素  

css主要通过三种方式添加到HTML中：  
+ 内联样式： 在HTML标签中使用style属性  
+ 内部样式表： 在HTML文档头部使用style元素来调用css  
+ 外部引用： 使用外部css文件  

#### 内联样式  
当特殊样式应用到个别元素时，可以在元素单独使用style属性  

```html
//这个例子定义了该段落的字体颜色，背景颜色，左边距的属性  
<p style="color: blue;background-color:gray;margin-left: 10px">this is a paragraph..</p>

//这个例子演示字体与对齐
<h1 style="font-family: Ani;font-size: 40px">A Title</h1>
<p style="text-align: center">使用text-align的属性替代center标签</p>
```  

#### 内部样式表  
当特殊样式应用到整个HTML文件时，可以使用内部样式表  
```html
<head>
<style type="text/css">
body{background-color: blueviolet}
p{color: aqua;font-size: 12px;text-align: center}

</style>
</head>


```  
#### 外部样式表  
当特殊样式应用到很多页面时，可以使用外部样式表，这个时候需要创建.css文件，然后在HTML头部使用link标签导入  
```html
<html>
<head>
<link rel="stylesheet" type="text/css" href="css文件路径/xx.css"> 
</head>
</html>
``` 
### css选择器  
css选择器可以理解为以什么样的方式选择某一部分空间进行css渲染  
主要有三类  

#### 构造选择器  
构造选择器针对网页中的一类标签叠加样式，一般形式为：  
```html
<style type="text/css">
    标签名 { 美化属性}
</style>
```  
这样本文件中所使用的所有该标签都按照设定的css样式进行渲染  

#### 类选择器  
类选择器针对某一类中的个别元素  
```html
<style type="text/css">
    .非关键字类名{ 美化属性}
</style>
```  
类选择器是自己命名的，但是不能够使用关键字，类选择器以点开头，调用方式为：  
```html
<li class="对应非关键字类名"/>
```  

#### id选择器  
id选择器类似类选择器，其实符号是井号#而不是点  ,一般与div配合应用于区域  
```html
<style type="text/css">
    #id名{ 美化属性}
</style>
<!--调用方式-->
<div id="id名">....</div>

```  

#### 盒模型  
+ 控件的margin：　外边距    ： 　
+ 控件的padding： 内边距
+ border： 边框  

控件居中：  

父元素 text-align:center  
子元素 display:inline-block  

#### 限制CSS ：  

```html
.lis li{
            list-style: none;
            float: left;
            padding-right: 20px;
        }
```  

对于lis类中的li标签进行更改  

#### 鼠标悬停更改：  

```html
h4:hover{
            color: brown;
        }
```  
对于h4这个标签，鼠标悬停时的动作，其他标签语法形式一样  
比如鼠标悬浮时更改背景图  

```html
.nav a:hover{
            background-color: blueviolet;
        }

<div class="nav">

    <a href="http://www.baidu.com" >baidu</a>
</div>
```  

对于使用nav标签下的超链接，鼠标悬浮时更改背景色  

#### css复用  

class里面可以写多个类，用空格区分；  


# 第二部分——JavaScript  
-----  

#### 特性
脚本语言，网页加载时解析；在用户端可以禁用  
在 JavaScript 中，用分号来结束语句是可选的。  

JavaScript 是脚本语言。浏览器会在读取代码时，逐行地执行脚本代码。而对于传统编程来说，会在执行前对所有代码进行编译。

#### 使用位置

+ 嵌入HTML时放在head里，用script标签,
```html
    <script type="text/javascript">
        document.write("print xxx");
        document.write("<h4>wangwangaw</h4>");
    </script>
```  

如果在文档已完成加载后执行 document.write，整个 HTML 页面将被覆盖：

script里面的标签受head中css style的限定；  

+ script可以放在head部分，也可以放在body部分  

```html
<head>
<script>
function myFunction()
{
document.getElementById("demo").innerHTML="My First JavaScript Function";
}
</script>
</head>
<p id="demo">A Paragraph</p>
<button type="button" onclick="myFunction()">Try it</button>

```  
其中getElementByID得到了id为demo的控件，即p，innerHTML方法是更改得到的控件的内容，再来看放在body部分实现的  

```html
<p id="demo">A Paragraph</p>

<button type="button" onclick="myFunction()">Try it</button>

<script>
function myFunction()
{
document.getElementById("demo").innerHTML="My First JavaScript Function";
}
</script>
```  

在body中创建脚本的区别是，只有当p对象载入后才能执行，更加严谨  

+ 也可以单独创建JavaScript文件，再导入  

```html
<!DOCTYPE html>
<html>
<body>
<script src="myScript.js"></script>
</body>
</html>
```

此时外部js代码中不再包含script标签  


+ prompt: 读取用户输入  
+ alert： 网页输出，强制型对话框，优先显示对话框内容  

```html
<button type="button" onclick="aaa()">button</button>
<script>
    function aaa() {
        window.alert("gugugu");
        document.write("<h1>gugugu</h1>");

    }
</script>
```  
改变HTML内容  
```html
x=document.getElementById("demo")  //查找元素
x.innerHTML="Hello JavaScript";    //改变内容
```  

在文本字符串中使用反斜杠对代码行进行换行
```javascript
document.write("Hello \
World!");
```
### 变量  

js使用var 关键字创建一个变量，变量类型是隐式的，通过赋值来限定数据类型，一般只关心数字和字符串两种  

变量声明却没有赋值的默认值是undefined,undefined表示没有值，而null表示值为null  

重新声明变量后值不会丢失，比如  

```javascript
var s = "gugugu";
var s;
```  

之后s的值仍然是字符串gugugu  
js中的变量是动态变量，可以通过不断赋值来改变类型；  
对于字符串的赋值双引号和单引号都可以，只要和字符串内部自带的引号区分开即可  
下面演示一些变量实例：  

```javascript
var answer="He is called 'Bill'";
var answer2='He is called "Bill"';

var x1=34.00;      
var x2=34;  
var y=123e5;      // 12300000
var z=123e-5;     // 0.00123

var xx=true
var yx=false

//创建数组#1
var arrs1 = new Array();
cars[0]="Audi";
cars[1]="BMW";
cars[2]="Volvo";

//#2
var cars2=new Array("Audi","BMW","Volvo");
//#3
var cars3=["Audi","BMW","Volvo"];
```

#### 对象  
对象由花括号分隔。在括号内部，对象的属性以名称和值对的形式 (name : value) 来定义。属性由逗号分隔：  

```javascript
var person={firstname:"Bill", lastname:"Gates", id:5566};
// 空格和折行无关紧要。声明可横跨多行：
var person={
firstname : "Bill",
lastname  : "Gates",
id        :  5566
};
```  

对象属性有两种寻址方式： 

```javascript
name=person.lastname;
name=person["lastname"];
```  

#### 函数  
函数在最开始的点击事件中就展示过，js中的函数用function 关键字声明，如果需要传参的话，要在括号中写上参数名字，不用声明类别  

```html
<button onclick="myFunction('Bill Gates','CEO')">点击这里</button>

<script>
function myFunction(name,job)
{
alert("Welcome " + name + ", the " + job);
}
</script>
```  
#### 作用域与生命周期  
在函数外声明的变量是全局变量，网页上的所有脚本和函数都能访问它。  
JavaScript 变量的生命期从它们被声明的时间开始。

局部变量会在函数运行以后被删除。

全局变量会在页面关闭后被删除。  

#### 运算符  

js大部分运算符与其他语言通用  
字符串可以用+连接  
如果把数字与字符串相加，结果将成为字符串  

逻辑运算符特殊的是有一个三等号===  
也同时有双等号==  
==是简单的等于，===是值和类型完全相等


#### windows对象属性  
+    JavaScript document 对象
+    JavaScript frames 对象
+    JavaScript history 对象
+    JavaScript location 对象
+    JavaScript navigator 对象
+    JavaScript screen 对象  

窗口属性  
对象事件  

日期数据中天数是1-31，而年月都是0到n-1