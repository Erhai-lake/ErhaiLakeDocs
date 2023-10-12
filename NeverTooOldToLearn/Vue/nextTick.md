# Vue异步更新和$nextTick

Vue是异步更新 DOM 的,想要在DOM更新完成之后做某件事,使用 **$nextTick**

**等 DOS 更新后**,才会触发执行此方法里的函数体

## 语法

`this.$nextTick(函数体)`