<template>
  <div class="container">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  data: function(){
      return{
          msg: '123'
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container{
  width: 100%;
  height: 30px;
  margin: 0 auto;
  background-color: blueviolet;
}

.container h1{
  margin-block-start: 0;
  margin-block-end: 0;
  width: 100%;
  height: 30px;
  margin: 0 auto;
  background-color: red;
}

</style>
