# Day3

- for循环

- Vue对象操作

  在⼀个实例中，通过调⽤另⼀个实例的属性，来操作其属性

```
var v1 = new Vue();
var v2 = new Vue({
 el:"#app2",
 data:{},
 methods:{
 changeTitle:function(){
 v1.title = "changed title";
 }
 }
});
```

