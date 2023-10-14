# ESlint代码规范

## 什么是代码规范

一套写代码的约定规则.

例如: "赋值符号的左右是否需要空格" "一句结束是否是要加;" ...

老话说: "**没有规矩不成方圆**" → 正规的团队需要 **统一** 的编码风格

[JavaScript Standard Style规范说明](https://standardjs.com/rules-zhcn.html)

一小部分

* 字符串使用单引号  'abc'
* 无分号  const name = 'zs'
* 关键字后加空格  if (name = 'ls') {...}
* 函数名后加空格  function name (arg) { ... }
* 坚持使用全等 === 摒弃 ==
* ...

## 如果不符合规范

如果你的代码不符合 standard 的要求,**ESlint** 会跳出来刀子嘴,豆腐心地提示你.

比如: 在main.js中随意做一些改动,添加一些分号,空行.

## 解决方法

### 手动修正
根据错误提示来一项一项 **手动** 修改纠正.

如果你不认识命令行中的语法报错是什么意思,根据错误代码去 [ESLint规则表](https://zh-hans.eslint.org/docs/latest/rules/) 中查找其具体含义.

### 自动修正

基于vscode插件 ESLint **高亮错误**,并 **通过配置** **自动** 帮助我们 **修复** 错误.