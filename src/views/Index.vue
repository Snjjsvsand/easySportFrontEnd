<template>
  <div id="index">
    <top-bar></top-bar>
    <top-list></top-list>
    <img src="~assets/img/index/bgc.png" alt="">
  </div>
</template>

<script>
import TopBar from 'components/content/topBar/TopBar'
import TopList from 'components/content/topList/TopList'
export default {
    name:'Index',
    components:{
      TopBar,
      TopList
    }

}
</script>

<style>
#index{
  height:3000px;
}
img{
  width:100vw;
}
</style>