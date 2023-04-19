# 基于Eslint的JS,TS,Vue3的代码校验

## 安装

`pnpm install eslint-config-ygxy -D`

## 说明

- ESLint：官方推荐库
- Vue3: 官方推荐插件库
- Vue官方基于typescript-eslint扩展库
- 自动导入Vue常规API，eslint检测配置
- 自定义规则
- Vue官方地址：[https://eslint.vuejs.org/rules/](https://eslint.vuejs.org/rules/)
- typescript-eslint官方地址：[https://typescript-eslint.io/linting/configs](https://typescript-eslint.io/linting/configs)

## 配合VSCode使用

- EsLint插件

```json
"prettier.enable": false, // 如果安装了prettier，需要禁用。否则冲突

// 开启eslint
"eslint.format.enable": true,
// 保存时执行格式化
"editor.formatOnSave": true,
"editor.codeActionsOnSave": {
    "source.fixAll": false,
    "source.fixAll.eslint": true,
},
// vue默认格式化工具
"[vue]": {
  "editor.defaultFormatter": "dbaeumer.vscode-eslint"
}
```

## 项目中使用

1. 项目根目录新建`.eslintrc.js`
2. 增加配置

    ```javascript
    module.exports = {
      extends: ['ygxy']
    }
    ```
