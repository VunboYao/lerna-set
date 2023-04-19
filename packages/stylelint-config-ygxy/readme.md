# 基于Stylelint的CSS语法校验库

## 安装

`pnpm install stylelint-config-ygxy -D`

## 说明

- 基于Stylelint的标准CSS语法校验
- CSS属性编写顺序校验
- Vue文件中CSS语法、属性顺序校验
- less,scss文件校验
- 常用缩进空格等规则

## 配合VSCode使用

```json
"editor.codeActionsOnSave": {
    "source.fixAll": false,
    "source.fixAll.stylelint": true,
},
"[css]": {
    "editor.defaultFormatter": "stylelint.vscode-stylelint"
  },
"[less]": {
  "editor.defaultFormatter": "stylelint.vscode-stylelint"
},
// stylelint CSS校验文件类型配置
"stylelint.validate": [
    "css",
    "less",
    "postcss",
    "scss",
    "sass",
    "vue"
]
```

## 项目中使用

1. 项目根目录新建`stylelint.config.js`
2. 增加配置

    ```javascript
    module.exports = {
      extends: ['stylelint-config-ygxy']
    }
    ```
