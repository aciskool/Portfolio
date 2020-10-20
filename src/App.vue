<template>
  <div>
  <link href="https://fonts.googleapis.com/css2?family=Fjalla+One&display=swap" rel="stylesheet">

  <HelloWorld></HelloWorld>
  <footer>{{footer}}</footer>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
  },
  methods: {
    setIndex(v){
      this.indexNo = v;
    }
  },
  data() {
    return {
      footer : "Made by Arvind using VueJS"
    }
  }
}
</script>

<style>
#app {
  font-family: 'Fjalla One', sans-serif;  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
body{
  margin: 0px; 
  background-color: lightyellow;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='4' height='4' viewBox='0 0 4 4'%3E%3Cpath fill='%23969d3e' fill-opacity='0.4' d='M1 3h1v1H1V3zm2-2h1v1H3V1z'%3E%3C/path%3E%3C/svg%3E");  
}
footer{
  background-color: black;
  color: white;
  text-align: center;
  padding: 1%;
  font-size: 20px;
}
</style>