<template> 
  <div class="main_data">
    <h1 style="text-align:left;">{{heading}}</h1>
    <p style="text-align:left;">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores eligendi deserunt harum? Repellendus nostrum rem nobis perferendis voluptatum, asperiores animi placeat quos eum ab sit fuga, aspernatur expedita voluptate at.</p>
  </div>
</template>

<script>
export default {
  name: 'MyDetails',
  props: {
    msg: String,
    heading: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .main_data{
    margin-left: 3%;
    margin-top: 15%;
  }
</style>
