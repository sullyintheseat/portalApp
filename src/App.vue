<template>
  <div id="app">
    <header>
      <span><img :src="require(`@/assets/${brand}.png`)" :class="`${brand}-logo`"></span>
    </header>
    <main>
      <img src="./assets/usta.png" alt="Vue.js PWA">
      <router-view></router-view>
    </main>
  </div>
</template>

<script>
import {storage} from './utils/storage'

export default {
  name: 'app',
  data () {
    return {
      brand: 'usta'
    }
  },
  mounted: function () {
    console.log(storage.getValue('test'))
  }
}
</script>

<style>
body {
  margin: 0;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

main {
  text-align: center;
  margin-top: 40px;
}

header {
  margin: 0;
  height: 56px;
  padding: 0 16px 0 24px;
  background-color: #fff;
  color: #ffffff;
  margin-top:2px;
  border-top:solid 1px #ddd;
  border-bottom:solid 1px #ddd;
}


header span {
  display: block;
  position: relative;
  font-size: 20px;
  line-height: 1;
  letter-spacing: .02em;
  font-weight: 400;
  box-sizing: border-box;
}
</style>
