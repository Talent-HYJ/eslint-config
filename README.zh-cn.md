# @heyuanjie/eslint-config 
 [![npm][npm-image]][npm-url] [![downloads][downloads-image]][downloads-url] [![javascript_code style][code-style-image]][code-style-url]

[ci-image]: https://github.com/Talent-HYJ/eslint-config/actions/workflows/release.yml/badge.svg?branch=master
[ci-url]: https://github.com/Talent-HYJ/eslint-config/actions/workflows/release.yml
[npm-image]: https://img.shields.io/npm/v/@heyuanjie/eslint-config.svg
[npm-url]: https://npmjs.org/package/@heyuanjie/eslint-config
[downloads-image]: https://img.shields.io/npm/dm/@heyuanjie/eslint-config.svg
[downloads-url]: https://npmjs.org/package/@heyuanjie/eslint-config
[code-style-image]: https://img.shields.io/badge/code__style-%40heyuanjie-brightgreen.svg
[code-style-url]: https://github.com/Talent-HYJ/eslint-config/

<div align='left'>
<a href="README.md">English</a> | <b>简体中文</b>
<br>
</div>

## 特性

- "双引号"，必须加分号;
- 格式化的自动修复（旨在独立使用，不需要Prettier）。
- TypeScript，Vue开箱即用
- 对 JSON、YAML、Markdown也支持格式化
- 导入自动排序，需要尾随逗号，更干净的提交差异
- 合理的默认值，最佳实践，只有一行的配置

## 如何使用

可共享的配置被设计在`.eslintrc`文件的`extends`。
你可以了解更多关于
[Shareable Configs](http://eslint.org/docs/developer-guide/shareable-configs) 在
官方ESLint网站上

###  运行以下命令开始使用:

### 安装

```bash
pnpm add -D eslint @heyuanjie/eslint-config
```

### 在你的`.eslintrc`文件中加入这个。

```json
{
  "extends": "@heyuanjie"
}
```

> 你通常不需要`.eslintignore`，因为它已经由预设提供了。

### 为package.json添加脚本配置

例如:

```json
{
  "scripts": {
    "lint": "eslint .",
    "lint:fix": "eslint . --fix"
  }
}
```

###  在Vscode中 配置自动修复

创建 `.vscode/settings.json`

```json
{
  "prettier.enable": false,
  "editor.formatOnSave": false,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
}
```

### 自定义规则

在你的`.eslintrc`文件中添加你喜欢的规则。

```json
{
  "extends": [
    "@heyuanjie"
  ],
  "rules": {
    "vue/component-tags-order": ["error", {
      "order": ["template", "script", "style"]
    }]
  }
}
```

## 徽章
在你的README中包括一个这样的徽章，以便让人们知道你的代码使用的是哪种ESLint样式。

[![heyuanjie-code-style-image](https://img.shields.io/badge/code__style-%40heyuanjie%2Feslint--config-brightgreen)](https://github.com/Talent-HYJ/eslint-config/)


[code-style-image]: https://img.shields.io/badge/code__style-%40heyuanjie%2Feslint--config-brightgreen
[code-style-url]: https://github.com/Talent-HYJ/eslint-config/

## 致谢
本项目基于 [@antfu/eslint-config](https://github.com/antfu/eslint-config)


