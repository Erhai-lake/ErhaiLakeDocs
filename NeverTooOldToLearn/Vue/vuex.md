# vuex

## 什么东西来的?

vuex 是一个 vue 的 **状态管理工具**,状态就是数据.

大白话: vuex是一个插件,可以帮我们 **管理vue通用的数据(多组件共享的数据)**

## 场景

1. 某个状态在 **很多个组件** 来使用(个人信息)
2. 多个组件 **共同维护** 一份数据(购物车)

## 优势

1. 共同维护一份数据,**数据集中化管理**
2. **响应式变化**
3. 操作简洁(vuex提供了一些辅助函数)

## 安装

1.安装 vuex

```sh
npm install vuex@next --save
```

2.新建 vuex 模块文件

新建 store/index.js 专门存放 vuex

```js
import Vue from 'vue'
import Vuex from 'vuex'
```

3.创建仓库

```js
Vue.use(Vuex)
```

```js
const store = new Vuex.Store()
```

```js
export default store
```

4.main.js 导入挂载

在 main.js 中导入挂载到 Vue 实例上

```js
import store from '@/store/index'
```

```js
fnew Vue({
	render: h => h(App),
	store
}).$mount ('#app')
```

## 提供数据

State 提供唯一的公共数据源,所有共享的数据都要统一放到 Store 中的 State 中存储.

在state对象中可以添加我们要共享的数据.

```js
const store = new Vuex.Store({
	// state状态，即数据，类似于vue组件中的data
	// 区别：
	// 1. data 是组件自己的数据
	// 2. state 是所有组件共享的数据
	state: {
		count: 101
	}
})
```

## 使用数据

### 提供 store 直接访问

获取 store:

1. `this.$store`
2. `import 导入 store`

模板中: `{{ $store.state.xxx }}`
组件逻辑中: `this.$store.state.xxx`
Js模板中: `store.state.xxx`


### 提供辅助函数(简化)

mapState是辅助函数,帮助我们把 store中的数据 **自动** 映射到 组件的计算属性中

1.导入mapState

```js
import {mapState} from 'vuex'
```

2.数组方式引入state

```js
mapState(['count'])
```

3.展开运算符映射

```js
computed: {
	...mapState(['count'])
}
```

## 修改数据

vuex 同样遵循单向数据流,组件中不能直接修改仓库的数据

```js
this.$store.state.count++
```

这个是错误代码(vue默认不会监测,监测需要成本)

通过 strict:true 可以开启严格模式 (有利于初学者,检测不规范的代码 => 上线时需要关闭)

我们应该通过 mutations 核心概念,就行修改数据
