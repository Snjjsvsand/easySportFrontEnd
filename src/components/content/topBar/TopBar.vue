<template>
  <div id = "top-bar-container">
    <div id="top-bar">
      <span id="title">
        <u>{{title}}</u>&nbsp;
        <strong>XUST</strong>
      </span>
    </div>
    <img id="top-banner" src="~assets/img/index/topbanner.png" alt />
  </div>
</template>

<script>
export default {
  name: "TopBar",
  props: {
    title: {
      type: String,
      default: "eSport now is a part of",
    },
  },
};
</script>

<style> 
#top-bar {
  height: 80px;
  line-height: 80px;
  width: 100%;
  background-color: #231f20;
  text-align: center;
}
#title *{
  color: white;
  font-size: 22px;
}
#top-banner {
  display: block;
  width: 100%;
}
strong{
    font-weight: 600;
    padding-left: 2px;
}
</style>