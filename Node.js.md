# Node.js

## 知识点

- node.js简介
  - JavaScript运行时工具
  - 既不是语言，也不是 框架，它是一个平台
- Node.js中的JavaScript
  - 没有BOM和DOM
  - EcmaScript基本的JavaScript语言部分
  - 在Node.js中为JavaScript提供了一些 服务器级别的API
    - 文件操作能力
    - http服务器的能力
- 模块
  - 核心模块
  - 第三方模块

##总结
- Node 中的JavaScript
  + EcmaScript
   * 变量
   * 方法
   * 数据类型
   * 内置对象
   * Array
   * Object
   * Date
   * Math
  + 模块系统
   *  在Node中没有 全局作用域的概念
   *  在Node中，可以通过require方法来加载执行多个JavaScript脚步文件
     - 模块完全封闭
     - 外部无法访问内部
     - 内部也无法访问外部
   *  模块作用域固然带来了一些好处，可以加载多个文件，可以完全避免变量命名冲突问题
   *  但是某些情况下，模块与模块之间是需要进行通信的，
   *  在每一个模块中，都提供了一个对象：`exports`
   *  该对象默认是一个空对象
   *  你要做的就是把需要被外部访问使用的成员手动挂载到`exports`接口对象中
   *  然后谁来`require`这个模块，谁就可以得到模块内部的`exports`接口对象

 + 核心模块
   * 核心模块是有Node提供的一个个的具名的模块，它们都有自己特殊的名称标识，例如
     - fs 文件操作模块
     - http 网络服务构建模块
     - os 操作系统信息模块
     - path 路径处理模块
     - 。。。。
   * 所有的核心模块都需要使用`require`方法来加载，然后才可以使用
   - `var fs = require('fs')`

- http
 + require
 + 端口号
   * ip 定位计算机
   * 端口号定位具体的应用程序
+ Content-Type
 * 服务器最好把每次响应的数据是什么内容类型都告诉客户端，而且要正确的告诉
 * 不同的资源对应的Content-Type是不一样的，可以参考：http://tool.oschina.net/commons
 * 对于文本类型的数据，最好加上编码，目的是为了防止中文乱码问题
+ 通过网络发送文件
 * 发送的并不是文件，本质上来讲发送的是文件的内容
 * 当浏览器收到服务器响应内容之后，然后根据你的Content-Type进行对应的解析处理

