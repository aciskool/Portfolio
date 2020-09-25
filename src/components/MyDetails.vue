<template> 
  <div class="main_data">
    <h1 style="text-align:left;" v-html="info[0].heading"></h1>
    <p style="text-align:left;" v-html="info[3].content"></p>
  </div>
</template>

<script>
export default {
  name: 'MyDetails',
  props: {
    msg: String,
    heading: String
  },
  methods: {
    myfunc: function(){
      console.log("id_selected");
    }
  },
  data(){
    return {
    info : [
        {id: 1,heading: "About Me", show: true, content: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores eligendi deserunt harum? Repellendus nostrum rem nobis perferendis voluptatum, asperiores animi placeat quos eum ab sit fuga, aspernatur expedita voluptate at."},
        {id: 2,heading: "Project", show: true, content:"<h1>Hello</h1>"},
        {id: 3,heading: "Education", show: true,  content:"<h1>Hello1</h1>"},
        {id: 4,heading: "Interests", shoe: true,  content:"<h1>Hello2</h1>"}    ]
    }
  }
}
</script>

<style scoped>
  .main_data{
    margin-left: 3%;
    margin-top: 5%;
  }
</style>
