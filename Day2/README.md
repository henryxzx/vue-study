# Day2

## Vue的虚拟DOM和diff算法
https://juejin.cn/post/6864108861290627080

### 虚拟DOM和真实DOM的区别？

- 虚拟DOM不会进行回流和重绘；
- 真实DOM在频繁操作时引发的回流重绘导致性能很低；
- 虚拟DOM频繁修改，然后一次性对比差异并修改真实DOM，最后进行依次回流重绘，减少了真实DOM中多次回流重绘引起的性能损耗；
- 虚拟DOM有效降低大面积的重绘与排版，因为是和真实DOM对比，更新差异部分，所以只渲染局部

### 分⽀语句

- v-if
- v-else-if
- v-else
- v-show: 实际上是让该元素的display属性为none,隐藏的效果。所以性能更好。

```
<div id="app">
 <p v-if="show">hahah</p>
 <p v-else>hohoho</p>
 <p v-show="show">hehehe</p>
 <input type="button" @click="show=!show" value="dianwo"/>
 </div>
 <script src="https://cdn.bootcss.com/vue/2.5.17-beta.0/vue.min.js"></script>
 <script>
 new Vue({
 el:"#app",
 data:{
 show:false
 }
 });
 </script>
```

通过模板标签对多个元素进⾏同⼀的if和else管理

```
<template v-if="show">
 <h1>heading</h1>
 <p>inside text</p>
 </template>
```

### 循环语句

```
<body>
 <div id="app">
 <ul>
 <li v-for="str in args">
 {{str}}
 </li>
 </ul>
 </div>
 <script src="https://cdn.bootcss.com/vue/2.5.17-beta.0/vue.min.js"></script>
 <script>
 new Vue({
 el:"#app",
 data:{
 args:["a","b","c","d"]
 }
 });
 </script>
 </body
```

```
<ul>
 <li v-for="(str,i) in args" :key="i">
 {{str}}{{i}}
 </li>
</ul>
```

```
<template v-for="(str,i) in args":key="i">
 <p>{{str}}{{i}}</p>
</template>
```



