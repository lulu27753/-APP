<template>
    
    <m-header title="豆瓣app" :bg="true">
      <a href="javascript:;" slot="left"><img class="m-icon-img" src="../assets/images/ic_bar_back_white.png"/>返回</a>
      <a href="javascript:;" slot="right">分享</a>
    </m-header>
  <!--   <m-header title="豆瓣app" :bg="true">
      <a href="javascript:;" slot="left"><img class="m-icon-img" src="../assets/images/ic_bar_back_white.png"/>返回</a>
      <a href="javascript:;" slot="right">分享</a>
    </m-header>
    <m-header title="豆瓣app" fixed>
      <a href="javascript:;" slot="left"><img class="m-icon-img" src="../assets/images/ic_bar_back_green.png"/>返回</a>
      <a href="javascript:;" slot="right"><img class="m-icon-img margin-right-10" src="../assets/images/ic_actionbar_search_icon.png"/></a>
      <a href="javascript:;" slot="right"><img class="m-icon-img" src="../assets/images/ic_chat_green.png"/></a>
    </m-header> -->
 
</template>

<script>
import mHeader from '../components/header'
  
  export default {
    name: 'Index',
    components: {
      mHeader
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
