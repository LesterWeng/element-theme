# element-theme

用于elementUI自定义主题及按需引入样式（搭配 `babel-plugin-component`）

操作步骤：
1. 执行`npm install`，安装两个依赖
2. 执行`et -i`，生成 `element-variables.scss` 文件，修改其中的scss变量
3. 执行`et`，生成theme文件
4. 修改`.babelrc`文件（或同样功能的文件），添加如下plugin(`styleLibraryName`为生成的theme文件夹相对于`.babelrc`文件的位置，需要加`~`)：
```js
"plugins": [
    [
      "component",
      {
        "libraryName": "element-ui",
        "styleLibraryName": "~src/styles/theme"
      }
    ]
  ]
```
