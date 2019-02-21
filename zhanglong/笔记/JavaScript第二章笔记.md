# JavaScript篇
* 第一章基本都是概念性的内容，不再多述。
* 我们从第二章开始学习，这一章开始在HTML文档中实际运用JavaScript，废话不多说，开始吧。

## 本章知识点如下：
* 1、使用<script>元素
* 2、嵌入脚本与外部脚本 
* 3、文档模式对 JavaScript的影响
* 4、考虑禁用 JavaScript的场景 

以前刚接触HTML的时候，学的是HTML4.0.1和VBScript，现在已经过时。像<center>、<font>、<script language = >等常用标签和语法已经被弃用，随后HTML5&&CSS3为我们提供了更为丰富多彩的视觉盛宴和实用功能。
1、JavaScript脚本可以直接写到HTML文档中，也可以以单独js文件的形式，使用类似<script type="text/javascript" src="path\*.js">的方法对其进行调用。（小知识点：按照惯例，外部 JavaScript文件带有.js扩展名。但这个扩展名不是必需的，因为 浏览器不会检查包含 JavaScript 的文件的扩展名。这样一来，使用 JSP、PHP 或其他 服务器端语言动态生成 JavaScript 代码也就成为了可能。但是，服务器通常还是需要 看扩展名决定为响应应用哪种 MIME 类型。如果不使用.js 扩展名，请确保服务器能 返回正确的 MIME类型）
2、如果我们在script标签中加入了src属性，代表着我们是调用的外部js文件。此时script标签中的JavaScript代码段会被浏览器忽略。
3、我们HTML文档中含有多个JavaScript段时，浏览器会自上而下进行解析，在第一个执行完毕后才会执行第二段代码。
4、传统来讲，JavaScript脚本都要放在<head>标签中，可是这样浏览器会优先下载JavaScript，之后显示页面内容。如果网络不太好，或者服务器或者浏览器有些问题，将会大大降低用户的浏览体验，所以我们最好把JavaScript代码段放到body标签即将结束的时候再加载，这样就会减少因为执行JavaScript而加载慢的页面。
5、在script标签中添加defer延迟标记，在HTML加载完毕后才会执行script代码段。
6、在script标签中添加async异步，只适用于外部脚本，告诉浏览器立即下载文件。添加async的script将会在页面load完毕之前执行。
7、在编写XHTML文档时，要比编写HTML时更加严谨。比如a > b，因为小于号旁边是空格，所以会导致解析错误，这时我们可以使用&lt代替小于号。当然也可以使用CData片段解决类似的问题。
8、<noscript>，很实用的一个标签。如果浏览器不支持script或者没有启用script功能，则会显示提示。