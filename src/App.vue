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
      footer : "Made by Arvind Chaudhary using Vue"
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
  background-color:#F5FFFA;
}
footer{
  background-color: black;
  color: white;
  text-align: center;
  padding: 1%;
  font-size: 20px;
}
</style>