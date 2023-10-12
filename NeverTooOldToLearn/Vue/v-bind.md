# v-bind

语法: `:class="对象/数组"`

1. **对象** → 键就是类名,值是布尔值.如果值为**true**,有这个类,否则没有这个类.
   1. `<div class="box" ：class="{类名1： 布尔值, 类名2： 布尔值}"></div>`
   2. 适用场景: 一个类名,来回切换
2. **数组** → 数组中所有的类,都会添加到盒子上,本质就是一个**class列表**.
   1. `<div class="box" ：class="[ 类名1, 类名2, 类名3 ]"></div>`
   2. 适用场景:批量添加或删除类

示例:

```html
<style>
	.active{
		background: #ff0000;
  		color: #fff;
	}
</style>

<div id="app">
	<ul>
		<li v-for="(item, index) in list" :key="item.id" @click="activeIndex = index">
			<a :class={ active: index === activeIndex } href="#">{{ item.name }}</a>
		</li>
	</ul>
</div>

<script src="https://cdn.jsdelivr.net/npm/vue@2.7.14/dist/vue.js"></script>

<script>
	const app = new Vue({
		el: '#app',
		data: {
			activeIndex: 0, // 记录高亮
			list: [
				{ id: 1, name: '京东秒杀'},
				{ id: 2, name: '每日特价'},
				{ id: 3, name: '品类秒杀'},
			]
		}
	})
</script>
```

## 增强

语法: `:style="样式对象"`

`<div class="box" ：style="{ CSS属性名1： CSS属性值, CSS属性名2： CSS属性值 }"></div>`

适用场景:某个具体的属性的动态设置