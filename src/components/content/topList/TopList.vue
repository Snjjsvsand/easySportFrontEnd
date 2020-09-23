<template>
  <div id="top-list">
    <div id="left-list">
      <span class="fade-anim">A easy-use campus sports meeting</span>
    </div>
    <div id="right-list">
      <div v-for="(item , index) in list" :key="index"  @mouseover = "hover(index)"  @mouseleave = "unhover(index)">
        <div>
          <div>
            <span class="fade-anim">{{item[0]}}</span>
          </div>
          <div class = "white-bgc"  v-show="listIndex[index]">
            <div v-for="(itemIn ,indexIn) in item" :key="indexIn" v-show = "indexIn!=0">
            <div>
              <span class="fade-anim pad-span">{{itemIn}}</span>
            </div>
          </div>

          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TopList",
  data() {
    return {
      list: [
        ["Products", "Pro", "Teams"],
        ["Pricing"],
        ["Documentation"],
        ["Community"],
      ],
      listIndex:[false,false,false,false]
    };
  },
  computed:{
    
  },
  methods:{
    hover(index){
      let newList = []
      for(let i = 0;i<4;i++){
        if(i == index){
          newList.push(true)
        }else{
          newList.push(false)
        }
      }
      this.listIndex = newList
      // console.log(this.listIndex[index])
    },
    unhover(index){
      let newList = []
      for(let i = 0;i<4;i++){
        newList.push(false)
      }
      this.listIndex = newList
      // console.log(this.listIndex[index])
    },
  }
};
</script>

<style>
#top-list {
  width: 100%;
  background-color: #ffffff;
  border-bottom: 1.5px solid rgb(229, 229, 229);
  height: 36px;
  line-height: 36px;
  padding: 8px 0;
  display: flex;
  justify-content: space-between;
}
#top-list > div {
  padding: 0 50px 0 0px;
  display: flex;
  width: 27vw;
  justify-content: space-evenly;
  cursor: pointer;
}

#top-list {
  font-size: 14px;
  font-family: sans-serif;
  font-weight: 600;
  letter-spacing: 0.015625em;
  padding: 10px;
}
#right-list {
  position: relative;
  font-weight: 600;
  /* background-color: #fff; */
  z-index: 999;
}
#left-list {
  font-weight: 400;
}
.fade-anim {
  transition: all 0.3s;
}
.fade-anim:hover {
  color: rgb(179, 179, 179);
}
.white-bgc{
  margin-left:-3px;
  position: absolute;
  background-color: white;
  display: block;
  /* padding: 5px 17px; */
  /* border:2px solid black; */
  border-radius:5px;
  box-shadow: 0 0 10px rgba(0,0,0,.3);
  /* left:-.5px ; */
}
.pad-span{
  padding: 5px 14px;
}

</style>