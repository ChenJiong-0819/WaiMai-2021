# 简介

本项目为一个前后端分离的外卖 Web App (SPA) 项目，包括商家, 商品, 购物车, 用户等多个子模块

## 1. 项目描述

1. 此项目为一个前后端分离的外卖 Web App (SPA) 项目
2. 使用了 Vue 全家桶+ES6+Webpack 等前端最新技术
3. 包括商家, 商品, 购物车, 用户等多个功能子模块
4. 采用模块化、组件化、工程化的模式开发

## 2. 能从此项目中学到什么?

### 2.1 项目开发流程及开发方法

1. 熟悉一个项目的开发流程
2. 学会组件化、模块化、工程化的开发模式
3. 掌握使用 vue-cli 脚手架初始化 Vue.js 项目
4. 学会模拟 json 后端数据，实现前后端分离开发
5. 学会 ES6+eslint 的开发方式
6. 掌握一些项目优化技巧

### 2.2 Vue 插件或第三方库

1. 学会使用 vue-router 开发SPA单页应用
2. 学会使用 axios/vue-resource 与后端进行数据交互
3. 学会使用 vuex 管理应用组件状态
4. 学会使用 better-scroll/vue-scroller 实现页面滑动效果
5. 学会使用 mint-ui 组件库构建界面
6. 学会使用 vue-lazyload 实现图片惰加载
7. 学会使用 mockjs 模拟后台数据接口

### 2.3 样式/布局/效果相关

1. 学会使用 stylus 编写模块化的 CSS
2. 学会使用 Vue.js 的过渡编写酷炫的交互动画
3. 学会制作并使用图标字体
4. 学会解决移动端 1px 边框问题
5. 学会移动端经典的 css sticky footer 布局
6. 学会 flex 弹性布局

## 3. API接口文档

[项目API接口文档](https://github.com/ChenJiong-0819/WaiMai-2021/blob/master/server/API%E6%96%87%E6%A1%A3.md) 

## 4. 运行项目

**先运行服务器，再打开项目**

开启服务端程序之前要先安装mongdb，并且成功打开数据库连接

**server文件夹下cmd命令：**

1. `npm install`
2. `npm start`

**工程根目录下cmd命令：**

1. `npm install`
2. `npm start`

**登陆**

1. 手机号登陆，需要自己注册容联云通讯后先添加一个测试账号，然后在server\util\sms_util.js中修改相应个人配置，之后输入符合格式的手机号即可
2. 密码登陆，默认用户名abc，密码123

**注意**

  1. vue cli关闭eslint： 
    在build文件夹打开webpack.base.conf.js 找到这一部分(config.dev.useEslint ? [createLintingRule()] : []) 
    修改 为这样 (config.dev.useEslint ? [] : []) 重新进行 npm start 就可以了
  2. 该项目因为使用的技术比较旧，向如安装stylus时，应该降低版本,建议安装stylus@0.54.5和stylus-loader@3.0.2
  3. 重复点击底部工具栏会报错
    
    1)是因为路由跳转没有catch  
    
    2)是因为chrome 监听touch类事件报错：无法被动侦听事件preventDefault，是新版本chrome 浏览器报错
    
   在FooterGuide.vue中goTo(path)中设置为 this.$router.replace(path).catch(err=>{}) 
   
   以及在App上的style中加入  *{ touch-action: pan-y }  
   
   
## 5. 演示截图
  ### 1.首页
![msite](./images/msite.PNG)
  ### 2.商家
![shop](./images/shop.PNG)
  ### 3.商品购物车
![shopCart](./images/shopCart.PNG)
  ### 4.个人中心
![profile](./images/profile.PNG)
  ### 5.登陆页面
![login](./images/login.PNG)
 
