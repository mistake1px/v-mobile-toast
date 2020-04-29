# v-mobile-toast

## 介绍

实现了一个简单的toast插件，调用方法

## 全局

``` bash
import Vue from 'vue'
import Toast from 'v-mobile-toast'
Vue.use(Toast)
```

OR

``` bash
import Vue from 'vue'
import { ToastPlugin } from 'v-mobile-toast'
Vue.use(ToastPlugin)
```

### 以插件形式注册时，使用方式为：

``` bash
this.$toast.show({})
this.$toast.hide()
```

## 组件

``` bash
import Toast from 'v-mobile-toast'
export default {
  components: {
    Toast
  }
}
```

## API

### 属性(以组件形式使用)

|参数 | 取值 | 必选 |说明
|---|----|---|---|
|value|true/false（默认）| 必选|控制显示隐藏 v-model|
|text|string| 必选|toast提示内容|
|time|number| 非必选 |toast显示的时长|
|type|string: success/warn/info| 非必选 |toast类型|
|width|string: 7.6em（默认）| 非必选 |toast宽度|
|is-show-mask|boolean: false(默认)/true| 非必选 |是否显示蒙层|

### 事件

|事件  |说明
|---|---|
|on-show|显示组件时触发|
|on-hide|隐藏组件时触发|

### 以插件形式调用时

``` bash
this.$toast.show({
  text: '',  // 必填
  // 除上面value之外的属性,
  // 事件，如果需要
  onShow: f, // 对应on-show
  onHide: f  // 对应on-hide
})

this.$toast.hide()
```
