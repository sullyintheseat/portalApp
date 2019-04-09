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
  position: absolute;
  z-index: 10000;
  margin: 0;
  margin-top: 4px;
  text-align: center;
  height: 56px;
  width: 100%;
  background-color: #fff;
  color: #fff;
  border-bottom: 1px solid #ddd;
  border-top: 1px solid #ddd;
  margin-bottom: 64px;
}

header span {
  box-sizing: border-box;
  text-align: center;
}
</style>
