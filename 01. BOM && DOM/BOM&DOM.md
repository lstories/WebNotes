# BOM && DOM
## BOM事件
- 事件就是用户或浏览器自身执行的某种动作, 事件可能是用户在某些内容上的点击, 鼠标经过某个特定元素或按下键盘上的某些按键. 事件还可能是Web浏览器中发生的事情, 比如说某个Web页面加载完成, 或是用户滚动窗口或改变窗口大小.
- 通过使用JavaScript, 你可以监听特定事件的发生, 并规定让某些事件发生以对这些事件做出响应
- JavaScript可以处理的事件类型为: 鼠标事件, 键盘事件, HTML事件

## 常见的BOM事件
- load: 当页面或图像加载完后, 立即触发
- blur: 元素失去焦点时触发
- focus: 元素获取焦点
- click: 鼠标点击某个对象
- change: 用户改变域的内容
- mouseover: 鼠标移动到某个元素上
- mouseout: 鼠标从某个元素上离开
- keyup: 某个键盘的键被松开
- keydown: 某个键盘的键被按下

## BOM事件处理程序
响应某个事件的函数就叫做事件处理程序(或事件侦听器). 事件处理程序的名字以 "on" 开头, 因此click事件的事件处理程序就是 onclick , 为时间指定处理程序的方式有好几种.

## BOM对象方法
这里主要说系统对话框:
- 浏览器通过(window对象的方法)alert(), confirm(), prompt()方法可以调用系统对话框向用户显示消息
- 消息框alert()(常用):
  - alert()方法用于显示带有一条指定消息和一个ok按钮的警告框
- 输入框prompt, 返回提示框中的值
  - prompt() 方法用于显示可提示用户进行输入的对话框
  - 参数(可选):
    - 第一个参数: 要在对话框中显示的纯文本
    - 第二个参数: 默认的输入文本
- 确认框confirm, 返回true/false
  - confirm() 方法用于显示一个带有指定消息和ok及取消按钮的对话框

## BOM对象
1. history
- history对象是历史对象, 包含用户(在浏览器窗口中)访问过的URL, history对象是window对象的一部分, 可以通过window.history属性对其进行访问
- history对象的属性: length, 返回浏览器历史列表中的URL数量
- history对象的方法:
  - back(): 加载history列表的前一个URL
  - forward(): 加载历史列表的下一个URL, 当页面第一次访问时, 还没有下一个url
  - go(number|URL): URL参数使用的时要访问的URL, 而number参数使用的是要访问的URL在History的URL列表中相对位置, go(-1), 到上一个页面

2. location
- location对象是window对象之一, 提供了与当前窗口加载的文档有关的信息, 还提供了一些导航功能, 也可以通过window.location属性来访问
- location对象的属性href: 设置或返回完整的URL
- location对象的方法
- reload(): 重新加载当前文档
- replace(): 用心的文档替换当前文档

3. document

## DOM?
- DOM: Document Object Model 文档对象模型
- 要实现页面的动态交互效果, BOM操作远远不够, 需要操作HTML才是核心, 如何操作HTML, 就是需要用到DOM
- DOM提供了用程序动态控制HTML的接口, DOM即文档对象模型描绘了一个层次的节点数, 运行开发人员添加, 移除或者是修改页面的某一部分, DOM处于JavaScript的核心地位上.
- 每个载入浏览器的HTML文档都会称为Document对象, document对象使我们考研从脚本中对HTML页面中的所有元素进行访问, Document对象是window对象的一部分, 可以通过window.document属性对其进行访问

## DOM节点
|  节点类型   | HTML类型  | 例如 |
|  ----  | ----  | ----|
| 文档节点  | 文档本身 | 整个文档document |
| 元素节点  | 所有的html元素 | ```<a><p><div>``` |
| 属性节点  | HTML元素内的属性 | id, href, name, calss |
| 文本节点  | 元素内的文本 | hello |
| 注释节点  | html中的注释 | ```<!-- -->``` |

## DOM获取节点
### 获取节点的四种方法
1. getElementById() -- 通过id属性值获取元素对象
2. getElementByName() -- 通过name属性值获取元素对象数组
3. getElementByClass() -- 通过class属性值获取元素对象数组
4. getElementByTagName() -- 通过元素名/标签名获取元素对象数组
5. 注意, 后三个获取的是数组, 所以需要通过数组下标取值

**注意:**  操作DOM节点是在等节点初始化完毕后, 才会执行  
**处理方式:**  
- 把script标签一道html末尾即可
- 使用onload事件来处理JS, 等待HTML加载完毕再加载onload事件里的JS

## DOM创建节点与插入节点



