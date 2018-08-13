# JavaScript

## 第1 章 JavaScript简介

JavaScript诞生于1995年, 当时的主要目的是处理以前由服务器语言负责的一些输入验证操作, 后来逐渐成为市面上浏览器必备功能. 如今JavaScript的用途早已不在局限于简单的数据验证, 而是具备了与浏览器窗口及其内容等几乎所有方便交互的能力. JavaScript已经成为了一门功能全面编程语言, 可以处理复杂的计算和交互, 拥有了闭包, 匿名函数, 甚至元编程等特性.

### 1.1 JavaScript简史

- 1995年2月 布兰登.艾奇(Brendan Eich)开发, 为搭Java顺风车, 临时把LiveScript改名为JavaScript. `JavaScript1.0`
- 随后网景发布了`JavaScript1.1`, 96年8月微软发布了JSscirpt
- 1997年(96年11月提交, 97年6月采纳), 以`JavaScript1.1`为蓝本的建议提交给了ECMA(European Computer Manufacturers Association欧洲计算机制造商协会), 协会指定39号技术委员会(TC39, Technical Committee 39 各大公司程序员)负责"标准化一种通用, 跨平台, 供应商中立的脚本语言的语法和语义", 数月后他们完成了ECMA-262. **定义了一种名为ECMAScript的新脚本语言的标准**
- 1998年, ISO/IEC(国际标准化组织和国际电工委员会)采用了ECMAScript作为标准即`ISO/IEC-16262`

### 1.2 JavaScript实现

JavaScript包含ECMAScript(核心),DOM(文档对象模型), BOM(浏览器对象模型)

---

#### 1.2.1 ECMAScript

ECMAScript与浏览器没有依赖关系, 因为她不包含输入和输出定义, ECMAScript只是语言的基础, 在此基础上可以构建更完善的脚本语言, 浏览器只是ECMAScript实现的 **宿主环境之一**

> 其他的宿主环境如: Node.js Adobe Flash

宿主环境提供ECMAScript的实现, 也提供扩展, 方便与环境交互.DOM,和BOM就是扩展

ECMAScript内容:

- 语法
- 类型
- 语句
- 关键字
- 保留字
- 操作符
- 对象

ECMAScript就是对实现该标准规定的各个方面的内容的语言的描述, JavaScript实现了ECMAScript

ECMAScript的不同版本以第`x`版表示, (描述特性实现的ECMA-262规范的第`x`个版本). 目前最近的一次大版本是第`6`版, 最流行的支持最广的是第`5`版

第二版是编辑加工的结果;

第三版是真正的修改更新, 还新增了正则, 第三版标志着ECMAScript成为一门真正的语言

第四版进行了检核修订, 以满足不断增长的Web开发需求, 但是由于改动太大, 几乎成为了一个新的语言, 正式发布前就被废弃了

第五版本来是tc39下属的一个小组, 名为ECMAScript 3.1 的小幅度改动, 后来正式取代tc39的方案, 在09年12月3日发布, 新增了很多更能, 以及严格模式 `strict`

第六版 是15年6月发布, 新的语言特性和概念

---

#### 1.2.2 文档对象模型(DOM)

Document Object Model是针对XML但经过扩展后, 用于HTML的应用程序编程接口(API Application Programming Interface). DOM把整个页面映射成为一个多层节点结构, HTML页面中的每个组成部分都是某种类型的节点, 这些节点又包含着不同类型的数据(树形图)

通过DOM创建的树形图, 开发人员获得了控制页面内容和结构的主动权, 借助DOM提供的API, 开发人员可以轻松的对节点增删改查.

`DOM 1级` 98年成为W3C的推荐标准: 由DOM核心和DOM HTML两个模块构成, 核心规定了如何映射基于XML的文档结构, 便于简化访问和操作, HTML是在核心的基础上加以扩展, 添加了针对HTML的对象和方法.

> DOM并不只针对JavaScript, 其他语言也有实现DOM的, 只不过在Web浏览器中, DOM已经成为了JavaScript重要组成部分.






## ES6

因为目前ES6尚未普及, 在开始试验ES6的时候, 需要配置Babel和Webpack两个工具来对ES6的内容进行编译和打包.

```shell
$ mkdir es6 # 创建项目文件夹
$ npm init -y # 初始化项目
$ npm install webpack@3.7.1 # 安装依赖包 webpack
$ npm install webpack-dev-server@2.9.1
$ npm install babel-core@6.26.0
$ npm install babel-loader@7.1.2
$ npm install babel-preset-env@1.6.0
```

完成项目搭建以后, 需要给项目构建配置文件, 首先是`webpack.config.js`

```JavaScript
//webpack.config.js
const webpack = require('webpack'); // 导入包

module.exports = { // 导出对象
  entry: './script.js', // 入口文件
  output: { // 输出对象 项目里可以嵌入这个输出的文件
    filename: './bundle.js'
  },
  module: { //使用的模块
    rules: [
      {
        test: /\.js?/, // 看是否是js文件
        exclude: /node_modules/, // 排除的js文件
        use: {
          loader: 'babel-loader', //使用这个来处理js文件
          options: { // 选项的一些预设
            presets: ['env'] 
          }
        }
      }
    ]
  }
}
```

然后再创建`.babelrc` 进行配置

```json
{
  "presets": ["env"]
}
```

然后在`package.json`里面添加脚本命令`start` 这样使用npm start就可以调用webpack的这个命令 创建一个本地的服务器, 

```json
{
  "script": {
  "start": "./node_modules/.bin/webpack-dev-server"
  }
}
```

然后再在项目创建`script.js`文件, 在这里文件里面可以编写项目或者练习脚本

最后在目录里创建`index.html`文件, 嵌入的脚本不是script.js 而是编译后的`bundle.js` 

最后运行实施工具

- $ npm start






