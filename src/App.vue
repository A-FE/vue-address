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
  name: 'app',
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
#app {
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
