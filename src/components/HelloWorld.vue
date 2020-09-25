<template>
  <div class="hello">
    <img src="../assets/a.png" alt="image" id="logo">

    <p id="heading"><b>Hi, I am Arvind. I am a Full Stack Developer.</b></p>

    <button v-on:click="giveMessage" id="bottom-button"><b>Learn More about me</b></button> 
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    giveMessage: function(){
      console.log("Hello");
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#logo{
  width: 60px;
  height: 60px;
}
#heading{
  font-size: 30px;
  color: black;
  margin-top: 10%;
}
#bottom-button{
  margin-top: 10%;
  font-size: 20px;
  background-color: white;
  outline: none;
  cursor: pointer;
}
#bottom-button :active{
  transform: translateY(4px);
}
</style>
