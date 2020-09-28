<template>
  <div class="hello-all">
    <div class="partition-header">
      <img src="../assets/a.png" alt="image" id="logo">
      <p id="heading"><b>Hi, I am Arvind <br>Welcome to my Portfolio!!</b></p>
    </div>
    <ul style="text-align:left;">
      <li v-for="item in NavList" :key="item.id" style="cursor:pointer;" v-on:click="changeIndex(item)"><a>{{item.heading}}</a></li>
    </ul>
    <div class="main_data">
        <div class="aboutme">
            <h1>About Me</h1>
            <div class="description">
              <p>I am a Full Stack Devloper interested in learning new Technologies & participate in development of awesome futuristic Products.</p>
            </div>
        </div>
        
  </div>
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
    },
    changeIndex: function(item){
      this.selected_index = item.id;
    }
  },
  data() {
    return {
      NavList : [
        {id: 1,heading: "About Me", show: true},
        {id: 2,heading: "Project", show: true},
        {id: 3,heading: "Education", show: true},
        {id: 4,heading: "Interests", shoe: true}
      ],
      selected_index : 1,
      info : [
        {id: 1,heading: "About Me", show: true, filename:"about.html",content: "<div><p>Hello</p></div>"},
        {id: 2,heading: "Project", show: true, content:"List of Projects"},
        {id: 3,heading: "Education", show: true,  content:"Education Background"},
        {id: 4,heading: "Interests", shoe: true,  content:"My interests for my future."}    
        ]
    }
  },
  loadHTML(){
    return "Hello";
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

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
  text-shadow: 0px -1px #ffffff;
  margin-top: 10%;
}
.description{
  border: 2px solid black;
  margin-right: 40%;
  padding: 2%;
  border-style: outset;
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
.main_data{
    margin-left: 3%;
    margin-top: 5%;
  }
</style>
