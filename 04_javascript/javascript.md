# JavaScript

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






