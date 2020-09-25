<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->

  <HelloWorld msg="Welcome"> </HelloWorld>

  <MyDetails msg="Name" heading="About Me"></MyDetails> 
</template>

<script>

import HelloWorld from './components/HelloWorld.vue';
import MyDetails from './components/MyDetails.vue';
// import uniqueId from 'lodash.uniqueid';

export default {
  name: 'App',
  components: {
    HelloWorld,
    MyDetails
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
