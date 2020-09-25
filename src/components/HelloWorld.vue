<template>
  <div class="hello-all">
    <div class="partition-header">
      <img src="../assets/a.png" alt="image" id="logo">
      <p id="heading"><b>Hi, I am Arvind <br>Welcome to my Portfolio!!</b></p>
    </div>
    <ul style="text-align:left;">
      <li v-for="item in NavList" :key="item.id"><a>{{item.heading}}</a></li>
    </ul>
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
  },
  data() {
    return {
      NavList : [
        {id: 1,heading: "About Me", show: true},
        {id: 2,heading: "Project", show: true},
        {id: 3,heading: "Education", show: true},
        {id: 4,heading: "Interests", shoe: true}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello-all{
  /* text-align: center; */
}
.partition-header{
  text-align: center;
  background: url(https://media.giphy.com/media/xT9IgN8YKRhByRBzMI/source.gif);
  /* background-repeat: no-repeat; */
  background-size: cover;
  padding: 10px;
}
#logo{
  width: 60px;
  height: 60px;
}
#heading{
  font-size: 30px;
  color: #000000;
  margin-top: 10%;
}
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

/* Change the link color to #111 (black) on hover */
li a:hover {
  background-color: #111;
}
</style>
