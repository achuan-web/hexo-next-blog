---
title: vite  [一个实验性的no build的vue开发服务器]
date: <code> +new Date() </code>
---
![](https://user-gold-cdn.xitu.io/2020/4/22/1719ebbc83be39f0?imageView2/1/w/1304/h/734/q/85/format/webp/interlace/1)

## 前言
在4月21日晚，Vue作者尤雨溪在哔哩哔哩直播分享了Vue.js 3.0 Beta最新进展。 里面尤大大所提到他最近在做的这个小工具 [vite](https://github.com/vuejs/vite) ,一个实验性的no build的vue开发服务器。(这个小工具可以支持热更新,且不用预编译)

*既然感兴趣那就着手试试，上手体验体验*

### 一丶安装

命令行复制以下

*  `mkdir vue-vite`  `新建文件夹`
*  `npm init -y`     `初始化项目`
*  `npm i vite -g`   `全局安装vite`

### 二丶新建文件

在项目目录下新建 一下文件

1. index.html 

```html
<div id="app"></div>
<script type="module" src="/main.js"></script>
```

2. Comp.vue 

```vue
<template>
  <button @click="count++">{{ count }}</button>
</template>

<script>
export default {
  data: () => ({ count: 0 })
}
</script>

<style scoped>
button { color: red }
</style>
```

3. main.js


```js
import { createApp } from 'vue'
import Comp from './Comp.vue'

createApp(Comp).mount('#app')
```

### 三丶启动


*  `cd vue-vite`    `进入目录`
*   `vite`         `启动项目`

1. 然后你就可以看到一下命令行启动提示了   

![](https://user-gold-cdn.xitu.io/2020/4/22/171a0286e01f540c?w=733&h=81&f=png&s=9855)

2. ctrl+鼠标左键点击进去看到这样的页面就代表你启动成功了   

![](https://user-gold-cdn.xitu.io/2020/4/22/171a02a53c93c15b?w=468&h=309&f=png&s=12012)

然后你可以尝试修改 `Comp.vue` 看看效果是不是那样神奇，不用预编译，且支持热更新

[vite地址 点这里](https://github.com/vuejs/vite)