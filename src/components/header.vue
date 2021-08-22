<template>
  <div class="container">
    <!-- <div class="circle">
      <a></a>
    </div> -->
    <div class="cup">
      <div class="wave1"></div>
      <div class="wave2"></div>
    </div>
    <div class="pipe"></div>

    <p>
      {{ 'eFafuCS' }}
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
  /* margin-left: 490px; */
  margin-left: 40%;
  left: 60px;
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

.cup {
  display: inline-block;
  position: absolute;
  background-color: #e9f5ff;
  border: 2px solid rgb(0, 0, 0);
  border-radius: 0 0 4px 4px;
  border-bottom: 25px;
  height: 45px;
  width: 30px;
  margin: 15px 430px;
  margin-left: 40%;
  display: flex;
  flex-direction: column;
  overflow: hidden;
  border: 2px solid rgb(102, 102, 102);
  transform: perspective(.5em) rotateX(-1.7deg);
  animation: water-wave linear infinite;
}

.cup::before {
  content: '';
  position: absolute;
  width: 6px;
  height: 40px;
  margin-left: 9px;
  margin-top: 2px;
  background-color: rgb(219, 219, 219);
  top: 0px;
}

.pipe {
  content: '';
  position: absolute;
  width: 6px;
  height: 8px;
  /* margin-left: 440px; */
  margin-left: 40%;
  left: 10px;
  margin-top: 4px;
  background-color: rgb(179, 179, 179);
  top: 0px;
  z-index: 1;
}

.wave1 {
    position: relative;
    top: 30%;
    left: -25%;
    background: rgb(189, 119, 38);
    opacity: .5;
    width: 50px;
    height: 100px;
    border-radius: 30%;
    animation: inherit;
    animation-duration: 5s;
}

.wave2 {
    position: absolute;
    top: 20%;
    left: -25%;
    background: rgb(255, 216, 133);
    opacity: .6;
    width: 50px;
    height: 50px;
    border-radius: 40%;
    transform: rotate(120deg);
    animation: inherit;
    animation-duration: 3s;
}

@keyframes  water-wave{
    0% {transform: rotate(0deg);}
    100% {transform: rotate(360deg);}
}

</style>
