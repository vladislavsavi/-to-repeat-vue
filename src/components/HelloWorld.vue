<template>
  <div class="hello">
    <h1>{{ current }}</h1>
    <ul>
      <li v-for="(item, index) in list" :key="index" v-on:click="pick(item.title)">{{ item.title }}</li>
    </ul>
  </div>
</template>

<script>
const mockData = [{
  title: '1'
}, {
  title: '2'
}, {
  title: '3'
}, {
  title: '4'
}]
export default {
  props: {
    change: Function
  },
  name: 'HelloWorld',
  data: function () {
    return {
      current: '1',
      list: mockData
    }
  },
  methods: {
    pick (value) {
      this.current = value
      this.change(`New title ${value}`)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
