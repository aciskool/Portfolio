<template>
  <div class="hello-all">
    <div class="partition-header">
      <img src="../assets/letterA.png" alt="image" id="logo">
      <p id="heading"><b>Hi, I am Arvind <br>Welcome to my Portfolio!!</b></p>
    </div>
    <ul style="text-align:left;" class="nav-bar">
      <li v-for="item in NavList" :key="item.id" style="cursor:pointer;" v-on:click="jumptoview(item)"><a>{{item.heading}}</a></li>
    </ul>
    <div class="main_data">
        <div class="aboutme" id="about">
            <h1><u>About Me:</u></h1>
            <div class="description">
              <p>{{description}}</p>
            </div>
            <div class="animation-images">
                <div class="buttons" v-for="data in buttonData" :key="data.id">{{data.name}}</div>
                  <div class="list-items">
                  <p v-for="data in frontend" :key="data.id">- {{data.name}} <span class="bar"><span class="progress" v-bind:style="{'background': red, 'width':data.value+'%'}"></span></span></p>
                </div>
                <div class="list-items">
                  <p v-for="data in backend" :key="data.id">- {{data.name}} <span class="bar"><span class="progress" v-bind:style="{'background': red, 'width':data.value+'%'}"></span></span></p>
                </div>
                <div class="list-items">
                  <p v-for="data in coding" :key="data.id">- {{data.name}}<span class="bar"><span class="progress" v-bind:style="{'background': red, 'width':data.value+'%'}"></span></span></p>
                </div>
            </div>
        </div>
        <div class="project" id="project">
            <h1><u>Project:</u></h1>
            <div class="projectData">
                <div v-for="data in project" :key="data.id" class="projectComponent">
                  <div style="font-size:25px"><strong>{{data.name}}</strong></div><br>
                  <div>{{data.about}}</div><br>
                  <div style="position:absolute;bottom:4%;"><button style="border:1px solid black;color:white;background-color:black;width:60px;height:30px;cursor:pointer;" @click="loadLink(data)"><strong>Link</strong></button></div>
                </div>
            </div>
        </div>
        <div class="education" id="education">
            <h1><u>Education:</u></h1>
            <div class="educationData">
                <div v-for="data in education" :key="data.id" class="educationComponent">
                    <div style="font-size:25px;"><strong><u>{{data.type}}</u></strong></div><br>
                    <div>{{data.school}}</div>
                    <div>({{data.time}})</div><br>
                    <div>{{data.major}}</div>
                    <div>{{data.agg}}</div>
                </div>
            </div>
        </div>
        <div class="contact" id="contact">
              <h1><u>Contact:</u></h1>
              <div>
                  
              </div>     
        </div>
  </div>
  </div>
</template>

<script>

export default {
  name: 'HelloWorld',
  methods: {
    giveMessage: function(){
      console.log("Hello");
    },
    jumptoview: function(item){
      var elmt = document.getElementById(item.ids);
      elmt.scrollIntoView({behavior: "smooth", block: "end", inline: "nearest"});
    },
    progressBar: function(){
      console.log("hello");
    },
    loadLink: function(data){
      if(data.id == 1)
        window.open("https://aravind-weather-app.herokuapp.com/");
    }
  },
  data() {
    return {
      description : "I am a Full Stack Developer interested in learning new Technologies & participate in development of awesome futuristic Products."
      ,
      NavList : [
        {id: 1,heading: "About Me", show: true , ids: "about"},
        {id: 2,heading: "Project", show: true , ids: "project"},
        {id: 3,heading: "Education", show: true , ids : "education"},
        {id: 4,heading: "Contact", shoe: true , ids : "contact"}
      ],
      selected_index : 1,
      info : [
        {id: 1,heading: "About Me", show: true, filename:"about.html",content: "<div><p>Hello</p></div>"},
        {id: 2,heading: "Project", show: true, content:"List of Projects"},
        {id: 3,heading: "Education", show: true,  content:"Education Background"},
        {id: 4,heading: "Interests", show: true,  content:"My interests for my future."}    
        ],
      frontend : [
        {id:1, name:"Angular", value:50},
        {id:2, name:"React", value:40},
        {id:3, name:"Vue", value: 65},
        {id:4, name:"HTML/CSS", value: 80},
      ],
      backend : [
        {id:1, name:"NodeJS", value:65},
        {id:2, name:"RESTful APIs", value:70},
        {id:3, name:"MySQL", value:80},
        {id:4, name:"SQLite", value:68}
      ],
      coding : [
        {id:1 , name: "C", value:70},
        {id:2 , name: "C++", value:75},
        {id:3 , name: "Python",value:55},
        {id:4 , name: "Javascript",value:60}
      ],
      buttonData : [
        {id:1 , name: 'Frontend'},
        {id:2, name: 'Backend'},
        {id:3, name: 'Coding'}
      ],
      project : [
        {id:1, name:"Weather Reporting Site", about:"I created a weather reporting Site that gives information regarding Temperature and Chances of Rain in an area. It is build by NodeJS and using Weather Forecast APIs."},
      ],
      education:[
        {id:1, type:"Graduation",school:"JSS Academy of Technical Education",time:"2016-2020",major:"Electronics & Communication",agg:"73%"},
        {id:2, type:"XII",school:"RSPS",time:"2014-2015",major:"Physics-Chemistry-Maths",agg:"91%"},
        {id:3, type:"X",school:"RSPS",time:"2012-2013",major:"Physics-Chemistry-Maths",agg:"9.8 CGPA"}
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
  width: 90px;
  height: 90px;
}
#heading{
  font-size: 30px;
  color: #ffffff;
  text-shadow: 4px 3px #000000;
  margin-top: 10%;
}
.description{
  border: 2px solid black;
  margin-right: 5%;
  padding: 2%;
  border-style: outset;
  font-size: 20px;
  text-align: center;
}
.projectData{
  display: grid;
  font-size: 19px;
  grid-template-columns: 1fr 1fr;
  grid-column-gap: 5%;
  padding: 10px;
  margin-bottom: 10%;
  margin-right: 5%;
  overflow: none;
}
.educationData{
  display: grid;
  font-size: 19px;
  grid-template-columns: 1fr 1fr 1fr;
  grid-column-gap: 5%;
  padding: 10px;
  margin-bottom: 10%;
  margin-right: 5%;
  overflow: none;
}
.projectComponent, .educationComponent{
    border: 1px solid black;
    padding: 10px;
    position: relative;
    height: 100%;
}
.educationComponent:hover , .projectComponent:hover{
  background-color: #F5F5F5;
}
.bar{
  border: 2px solid black;
  float:right;
  width: 40%;
  height: 15px;
  margin-right: 10%;
  background-color: grey;
  overflow: hidden;
}
.progress{
  border-right: 2px solid black;
  float: left;
  padding: 2px;
  height: 15px;
  background-color: white;
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
  .animation-images{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    padding: 5%;
  }
 .buttons{
    text-align: center;
    background-color: #ba4d02;
    font-family: 'Fjalla One', sans-serif;
    color: white;
    padding: 5%;
    font-size: 28px;
    margin-right: 10%;
    border: 1px white solid;
 }
 .buttons:hover{
   background-color: #4a3323;
 }
 .list-items{
   font-size: 20px;
 }
</style>
