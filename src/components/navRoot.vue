<template>
  <div class="container">
      <nav-top></nav-top>
      <nav-top></nav-top>
      <nav-top></nav-top>
      <nav-top></nav-top>
      <nav-top></nav-top>
      <nav-top></nav-top>
      <nav-top></nav-top>
      <nav-top></nav-top>
      <nav-top></nav-top>
  </div>
</template>

<script>
import navTop from './navigationBar/navTop.vue';

export default {
    components: {
        'nav-top':navTop
    },
    data: function(){
        return{

        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container{
  width: 80%;
  height: 800px;
  margin: 0 auto;
  background-color: rgb(48, 131, 76);
  padding-top: 50px;
}



</style>
