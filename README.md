# vue-address
> 基于vue.js的多级联动地址选择器，需要配合element-ui使用
* [源码](https://github.com/peng1992/vue-address)
* [在线DOM](https://peng1992.github.io/vue-address/)

#### 如何使用？

	<template>
      <div id="app">
        <img src="./assets/logo.png">
        <vue-address
            :province="province"
            :city="city"
            :detail="detail"
            @change="handlerChange"
        ></vue-address>
      </div>
    </template>

    <script>
    import vueAddress from './components/address'
    export default {
      components: {
        vueAddress
      },
      data: function() {
        return {
            province:'',
            city:'',
            detail:''
        }
      },
      methods: {
        handlerChange: function (val) {
            console.log(val);
        }
      }
    }
    </script>
    <style>
    #app {text-align: center;color: #2c3e50;margin-top: 60px;}
    </style>

#### vue-address属性
* province	省
* city      市
* detail    详细地址

#### vue-address事件
* change  当省、市、详细地址任一值改变时触发