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
<td>1</td>
<td>2</td>
<td>3</td>
</tr>

</table>


```

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

//在新页面打开链接，只需将target设置为_blank
<a href="xxxxxx" target="_blank">新页面打开</a>

```
#### 实际开发中常用的四种块状结构  
+   
**万维网制定规范标准**
+ 标签名属性名必须小写  
+ 标签必须关闭  
+ 属性值必须用引号  
+ 标签必须正确嵌套
+ 必须添加文档类型声明 