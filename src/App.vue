<template>
  <div id="app">
    <img src="./assets/logo.png">
    <hello v-for="(car,index) in cars" :key="'car-'+index" :data="{ ...car, date: '20-12-2018'}"></hello>
  </div>
</template>

<script>
import Hello from './components/Hello'

export default {
  name: 'app',
  data () {
    return {
      cars: [{'title': 'title1'}, {'title': 'title2'}, {'title': 'title3'}]
    }
  },
  components: {
    Hello
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
