<template>
  <div class="container">
    <div class="circle">
      <a></a>
    </div>
    <p>
      {{ 'CS Nav' }}
    </p>
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
  height: 70px;
  margin: 0 auto;
  background-color: rgb(255, 255, 255);
}

.container p {
  margin-left: 230px;
  margin-top: 15px;
  position: relative;
  display: inline-block;
  vertical-align: middle;
  font-family:-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  font-size: 35px;
  font-weight: 600;
  line-height: 35px;
}

.circle {
  display: inline-block;
  position: absolute;
  left: 150px;
  top: 5px;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  border: 5px solid transparent;
  border-top-color: rgb(221, 80, 68);
  /* border-top: 4px solid rgb(221, 80, 68); */
  animation: spin 2.5s linear infinite;
}

.circle a {
  margin-left: 14px;
  margin-top: 12px;
  max-width: 25px;
  width: 26px;
  height: 26px;
  vertical-align: middle; 
  background-image: url('../assets/ima/logo_center.png');
  background-repeat:no-repeat;
  background-size:26px 26px;
  display: inline-block;
  position: relative;
  animation: center 2.5s linear infinite;
  border: 2px;
}

.circle::before {
  content: '';
  position: absolute;
  top: 0px;
  left: 0px;
  right: 0px;
  bottom: 0px;
  border-radius: 50%;
  border: 5px solid transparent;
  border-top-color: rgb(255, 205, 67);
  /* border-top: 4px solid  rgb(255, 205, 67); */
  /* border-left-color:  rgb(255, 205, 67); */
  animation: spin 2s linear infinite;
}

.circle::after {
  content: '';
  position: absolute;
  top: 5px;
  left: 5px;
  right: 5px;
  bottom: 5px;
  border-radius: 50%;
  border: 5px solid transparent;
  animation: spin 3.5s linear infinite;
  border-top-color: rgb(69, 157, 245);
  /* border-top: 4px solid rgb(28, 162, 97);
  border-left: 4px solid rgb(28, 162, 97); */
  /* border-left-color: rgb(28, 162, 97); */
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

@keyframes center {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(-360deg);
  }
}

</style>
