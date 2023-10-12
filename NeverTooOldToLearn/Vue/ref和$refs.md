# ref 和 $refs

## 作用

利用ref和 $refs可以用于 **获取 dom 元素**，或 **组件实例**

## 特点

查找范围 → **当前组件内(更精确稳定)**

### 获取 dom

1.目标标签 - 添加 ref 属性

```html
<div ref="chartRef">我是渲染图表的容器</div>
```

2.恰当时机,通过this.$refs.xxx,获取目标标签

```js
mounted () {
	console.log(this.$refs.charRef)
}
```

### 获取组件

1.目标标签 - 添加 ref 属性

```html
<BaseForm ref="baseForm"></BaseForm>
```

2.恰当时机,通过this.$refs.xxx,获取目标标签,就可以 **调用组件对象里面的方法**

```js
this.$refs.baseForm.组件方法()
```
