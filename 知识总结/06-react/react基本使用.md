## react常用vs code插件：

1. JavaScript (ES6) code snippets
2. React-Native/React/Redux snippets for es6/es7
3. Reactjs code snippets
4. Auto Close Tag
5. Auto Rename Tag





## react基本使用

例如：一个小的dome项目 流程如下：

**1.初始化项目**

```javascript
# npm init -y                      // -y 是 yes 的意思
```

**2.安装react**

```javascript
# npm i react react-dom
```

**3.在创建的文件夹(dome)里面，引入react 和 react-dom 两个 js 文件** 

```javascript
<script src="./node_modules/react/umd/react.development.js"></script> 
<script src="./node_modules/react-dom/umd/react-dom.development.js"></script> 
```

`方法说明`

 1. React.createElement() 说明（知道） 

    - 返回值：React元素 
    - 第一个参数：要创建的React元素名称 
    - 第二个参数：该React元素的属性 
    - 第三个及其以后的参数：该React元素的子节点 

 2. ReactDOM.render() 说明 

    - 返回值:React元素

    - 第一个参数：要渲染的React元素 
    - 第二个参数：DOM对象，用于指定渲染到页面中的位置 

**dome 演示案例如下：**

```javascript
<body>
    
  <!-- 
    react作用：它是一个用于构建用户界面的JavaScript库。
   -->

  <!-- 1.创建一个容器-->
  <div id="app"></div>



  <!-- 2.引入
    react       核心包，提供创建元素、组件等功能；
    react-dom   操作DOM、提供 DOM 相关功能
  -->
  <script src="./node_modules/react/umd/react.development.js"></script>
  <script src="./node_modules/react-dom/umd/react-dom.development.js"></script>
  

  
  <!-- 3.写 react   JS -->
  <script>
    // 参数1：标签的名称
    // 参数2：元素的属性
    // 参数3：要渲染的内容,第三个及其以后的参数，都是该元素的子节点
    const h1 = React.createElement('span', null, 'h1');     // react 元素已经创建完成
    const h2 = React.createElement('h2', null, 'hello');
    const div = React.createElement('div', {className: 'test', style:{color: 'red'}}, h1,h2);
    ReactDOM.render(div, document.getElementById('app'));    // 渲染到容器里面
  </script>
</body>
```

