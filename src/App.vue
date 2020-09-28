<template>
  <link href="https://fonts.googleapis.com/css2?family=Fjalla+One&display=swap" rel="stylesheet">
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->

  <HelloWorld></HelloWorld>

  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  methods: {
    setIndex(v){
      this.indexNo = v;
    }
  }
}
</script>

<style>
#app {
  font-family: 'Fjalla One', sans-serif;  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 60px;
  margin: 0px;
}
body{
  margin: 0px; 
  background-color:#F5FFFA;
}
</style>