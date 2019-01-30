---
title: vue 后记
date: 2019-01-25 15:56:38
tags: vue
categories: vue
---

## Vue.extend构造器
>vue.extend（构造器）类似于组件,data选项是特例（data是一个函数）,创建完成之后使用`$mount()`挂载到标签上


## Vue.filter过滤器
>用在`v-bind`中或者`花括号中`,写在尾部用管道符隔开` | `


>一个组件的 `data` 选项必须是一个`函数`


## Vue.compile渲染函数
>相当于在当前实例上渲染一个dom的结构,当这个实例的el属性挂载到标签上的时候就会渲染这个dom结构
```
var res = Vue.compile('<div><span>{{ msg }}</span></div>')

new Vue({
  data: {
    msg: 'hello'
  },
  render: res.render,
  staticRenderFns: res.staticRenderFns
})

```

