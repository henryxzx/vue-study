# Day1

## 介绍Vue.js

官网说的很清楚，不多bb了

Vue (读音 /vjuː/，类似于 **view**) 是一套用于构建用户界面的**渐进式框架**。与其它大型框架不同的是，Vue 被设计为可以自底向上逐层应用。Vue 的核心库只关注视图层，不仅易于上手，还便于与第三方库或既有项目整合。另一方面，当与[现代化的工具链](https://vuejs.bootcss.com/guide/single-file-components.html)以及各种[支持类库](https://github.com/vuejs/awesome-vue#libraries--plugins)结合使用时，Vue 也完全能够为复杂的单页应用提供驱动。

https://vuejs.bootcss.com/guide/index.html



## cha值表达式

https://vuejs.bootcss.com/guide/index.html#%E5%A3%B0%E6%98%8E%E5%BC%8F%E6%B8%B2%E6%9F%93



## 事件绑定和属性绑定

常用缩写

### [`v-bind` 缩写](https://vuejs.bootcss.com/guide/syntax.html#v-bind-缩写)

```
<!-- 完整语法 -->
<a v-bind:href="url">...</a>

<!-- 缩写 -->
<a :href="url">...</a>

<!-- 动态参数的缩写 (2.6.0+) -->
<a :[key]="url"> ... </a>
```

### [`v-on` 缩写](https://vuejs.bootcss.com/guide/syntax.html#v-on-缩写)

```
<!-- 完整语法 -->
<a v-on:click="doSomething">...</a>

<!-- 缩写 -->
<a @click="doSomething">...</a>

<!-- 动态参数的缩写 (2.6.0+) -->
<a @[event]="doSomething"> ... </a>
```

https://vuejs.bootcss.com/guide/syntax.html#%E5%8F%82%E6%95%B0