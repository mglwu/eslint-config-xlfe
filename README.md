# eslint-config-xlfe

### 使用

#### eslint-config-xlfe

第一步安装依赖

```bash
npm install --save-dev eslint eslint-config-xlfe @babel/core @babel/eslint-parser 
```

第二步在 .eslintrc 文件中添加以下代码

```
{
  "extends": ['xlfe']
}
```

#### eslint-config-xlfe/vue

第一步安装依赖

```bash
npm install --save-dev eslint @babel/eslint-parser vue-eslint-parser eslint-plugin-vue eslint-config-xlfe
```

第二步在 .eslintrc 文件中添加以下代码

```
{
  extends: [
    'xlfe',
    'xlfe/vue'
  ]
}
```

### 注意事项

此规则只约束代码中可能的错误或逻辑错误有关，关于代码风格自行安装 Prettier 插件。

#### Prettier 配置

```js
module.exports = {
  // 一行最多 120 字符
  printWidth: 120,
  // 使用 2 个空格缩进
  tabWidth: 2,
  // 不使用缩进符，而使用空格
  useTabs: false,
  // 行尾需要有分号
  semi: false,
  // 使用单引号
  singleQuote: true,
  // 对象的 key 仅在必要时用引号
  quoteProps: 'as-needed',
  // jsx 不使用单引号，而使用双引号
  jsxSingleQuote: false,
  // 末尾需要有逗号
  trailingComma: 'none',
  // 大括号内的首尾需要空格
  bracketSpacing: true,
  // jsx 标签的反尖括号需要换行
  bracketSameLine: false,
  // 箭头函数，只有一个参数的时候，不需要括号
  arrowParens: 'avoid',
  // 每个文件格式化的范围是文件的全部内容
  rangeStart: 0,
  rangeEnd: Infinity,
  // 不需要写文件开头的 @prettier
  requirePragma: false,
  // 不需要自动在文件开头插入 @prettier
  insertPragma: false,
  // 使用默认的折行标准
  proseWrap: 'preserve',
  // 根据显示样式决定 html 要不要折行
  htmlWhitespaceSensitivity: 'css',
  // vue 文件中的 script 和 style 内不用缩进
  vueIndentScriptAndStyle: false,
  // 换行符使用 lf
  endOfLine: 'lf',
  // 格式化内嵌代码
  embeddedLanguageFormatting: 'auto'
}
```

#### editorconfig 配置

```bash
root = true

[**]

# 编码格式
charset = utf-8

# 文件结尾符
end_of_line = lf
insert_final_newline = true

# 去除行尾空白字符
trim_trailing_whitespace = true

# space 缩进
indent_style = space
indent_size = 2

[*.md]
trim_trailing_whitespace = false

[{package.json,.babelrc,.eslintrc}]
indent_style = space
indent_size = 2

[*.yml]
indent_style = space
indent_size = 2
```
