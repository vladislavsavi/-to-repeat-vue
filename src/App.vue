<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>{{ title }}</h1>
  <HelloWorld :change="changeTitle"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data () {
    return {
      title: 'old'
    }
  },
  methods: {
    changeTitle (value) {
      this.title = value
    }
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
  margin-top: 60px;
}
</style>
