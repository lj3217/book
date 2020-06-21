## rem

一、postcss-pxtorem将px转为rem

* 安装：

```javascript
npm install postcss-pxtorem -D
```

创建postcss.config.js文件夹

* 添加如下代码

```javascript
module.exports = {
  plugins: {
    autoprefixer: {
      browsers: ['Android >= 4.0', 'iOS >= 8'],
    },
    'postcss-pxtorem': {
      rootValue: 37.5,
      propList: ['*'],
    }
  }
}
```

* 重启服务



二、使用 amfe-flexible 动态设置rem基准值

安装：

```javascript
npm install amfe-flexible
```

然后在 main.js 中新增：

```javascript
import 'amfe-flexible/index.js'
```

