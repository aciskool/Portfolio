<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->

  <HelloWorld msg="Welcome"> </HelloWorld>

  <MyDetails></MyDetails> 
</template>

<script>

import HelloWorld from './components/HelloWorld.vue';
import MyDetails from './components/MyDetails.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    MyDetails
  },
  data(){
    return {
      selected_index: 1
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 60px;
  margin: 0px;
}
body{
  margin: 0px; 
}
</style>
