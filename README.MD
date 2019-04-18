## 基于gulp搭建的前端自动化构建

**快速构建前端项目框架。比如官网类小demo测试等**
**如果是移动端需要使用基础的basic-m.css，和base.scss还有公用头使用header-m.html模板**
**可以随便根据自己的要求去进行修改配置**

## 项目启动
```
// 常用命令
开发环境： npm run dev
生产环境： npm run build

// 单任务命令
执行压缩： gulp zip
编译页面： gulp html
编译脚本： gulp script
编译样式： gulp styles
语法检测： gulp eslint
压缩图片： gulp images
```



## 项目目录
```
├── README.md         # 项目说明
├── config            # gulp路径配置
├── dist              # 打包路径
|
├── gulpfile.js       # gulp配置文件
├── package.json      # 依赖包
|
├── src               # 项目文件夹
│   ├── include       # 公用页面引入
│   ├── static        # 资源文件夹
│   │   ├── images    # 图库
│   │   ├── js        # 脚本
│   │   └── styles    # 样式（scss, css）
│   └── views         # 页面
└── webpack.config.js # webpack配置文件
```

## 项目配置
1、 使用严格的 eslint 规范 [文档链接](https://github.com/airbnb/javascript)
* 如果不想使用eslint，可以gulpfile文件中去掉该任务

2、使用scss预处理
* 可以根据个人喜好，去配置不同的预处理工具

3、es6转es5



## 代理模式
* config/index.js文件中配置

**例子如下**
``` javascript
 middleware: proxyMiddleware('/api', {
      target: 'http://xxx',
      changeOrigin: true,
      logLevel: 'debug',
  })
```

## 使用Eslint 
config/index.js文件
```
useEslint: false // 是否启用eslint
```

## 使用webpack
* 集成webpack功能，可以自行选择

config/index.js文件
```
useWebpack: false // 是否启用webpack
```







