<template>
  <m-tabbar>
    <m-tabbar-item id="tab1"><img src="../assets/images/ic_tab_home_normal.png" alt="" slot="icon-normal"> 首页</m-tabbar-item>
    <m-tabbar-item id="tab2"><img src="../assets/images/ic_tab_subject_normal.png" height="96" width="96" alt="" slot="icon-normal">书影音</m-tabbar-item>
    <m-tabbar-item id="tab3"><img src="../assets/images/ic_tab_status_normal.png" alt="" slot="icon-normal">广播</m-tabbar-item>
    <m-tabbar-item id="tab4"><img src="../assets/images/ic_tab_group_normal.png" height="96" width="96" alt="" slot="icon-normal">小组</m-tabbar-item>
    <m-tabbar-item id="tab5"><img src="../assets/images/ic_tab_profile_normal.png" alt="" slot="icon-normal">我的</m-tabbar-item>
  </m-tabbar>
</template>

<script>
import mTabbar from '../components/tabbar'
import mTabbarItem from '../components/tabbar-item'
export default{
  name:'index',
  components:{
    mTabbar,
    mTabbarItem
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
