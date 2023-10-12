# .sync修饰符

## 作用

可以实现 **子组件** 与 **父组件数据** 的 **双向绑定**,简化代码

## 特点

prop属性名,可以 **自定义**,非固定为 **value**.

## 场景

封装弹框类的基础组件,**visible属性** true显示 false隐藏

## 本质

就是 **：属性名和** **@update：属性名** 合写

## 父组件 (使用)

```html
<BaseDialog :visible.sync="isShow">

<BaseDialog :visible.sync="isShow" @update:visible="isShow = $event">
```

## 子组件 (封装)

```js
props: {
	visible: Boolean
},
this.$emit('update:visible', false)
```