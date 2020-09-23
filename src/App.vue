<template>
  <div id="app">
    <index></index>
  </div>
</template>

<script>
import Index from 'views/Index'

export default{
  name:'App',
  components:{
    Index
  }

}
</script>
<style >
*{
  font-family: 'Source Sans Pro', 'Lucida Grande', sans-serif;
  margin:0;
  padding:0;  
}
#app{
  width: 100%;
  overflow: hidden;
}
</style>

