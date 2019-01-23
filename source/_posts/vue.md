---
title: vue
date: 2019-01-22 22:55:53
updated: 2019-01-22 23:11:59
tags: vue
categories: vue
---

![你想要输入的替代文字](vue/vue.jpg)

## 动态绑定图片无法加载
- 图片的绑定需要使用v-bind:src
- 在data中用require("")引入图片路径
- 把图片放在static中

vue 权威指南
>链接: https://pan.baidu.com/s/1WCUp2lz1bUc-oTiohUFHPw 提取码: 9b8u

## 三种前端架构模式
1. mvvm  model（模型）-viewModel（）-view（视图）
>viewModel 实现了observe（类似观察者模式）
2. mvc  
3. mvp

## v-model修饰符
1. lazy 只有文本框的on-change触发后值才会发生改变
2. number 将输入的值转为number类型
3. trim 去掉输入的字符串后的空格


> 使用`v-for`的时候必须绑定一个`key`,为了区分每一项

> 我们应当尽量避免给已经`v-model`的数组赋值，如果需要复制的话，请使用`$set`

## vue绑定class
```
HTML代码：
<div :class="{ 'class-a': isA, 'class-b': isB}">Demo4</div>

Javascript代码：
data: {
  isA: false,  //当isA改变时，将更新class
  isB: true    //当isB改变时，将更新class
}
渲染后的HTML:
<div class="class-b">Demo4</div>

```

```
HTML代码：
<div :class="objectClass">Demo5</div>

Javascript代码：
data: {
  objectClass: {
    class-a: true,
    class-b: false
  }
}

渲染后的HTML:
<div class="class-a">Demo5</div>

```
```
HTML代码：
<div :class="[classA, classB]">Demo6</div>

Javascript代码：
data: {
  classA: 'class-a',
  classB: 'class-b'
}

渲染后的HTML:
<div class="class-a class-b">Demo6</div>

```

![你想要输入的替代文字](vue/style.png)

## vue绑定style
```
<div :style="{ fontSize: size + 'px' }"></div>

```















