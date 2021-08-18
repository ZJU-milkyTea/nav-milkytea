<template>
  <div class="container">
    
    <!-- 用父子传message的形式来决定每个nav的子nav中的图片和链接跳转放哪个， 最子的NAV通过message来选择图片和链接 -->

    <nav-top :message="0">

    </nav-top>

  </div>
</template>

<script>
import navTop from './navigationBar/navChild.vue';

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
  width: 85%;
  height: 800px;
  margin: 0 auto;
  background-color: rgb(236, 236, 236);
  padding-top: 50px;
}



</style>
