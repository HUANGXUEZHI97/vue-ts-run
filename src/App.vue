<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/> -->
    <button @click="increment">+</button>
    {{count}}
    <button @click="decrement">-</button>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

// 注册Components
@Component
export default class App extends Vue {
  // class属性即是组件的data
  count = 0

  // class的方法即是组件的methods
  increment () {
    this.count++
  }

  decrement () {
    this.count--
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
