<template>
  <div id="app">
    <v-head></v-head>
    <through-ad></through-ad> 
    <index></index>
    <v-foot></v-foot>
  </div>
</template>

<script>
import vHead from "./components/head/vHead";
import throughAd from "./components/common/throughAd";
import index from "./components/page/index";
import vFoot from "./components/foot/vFoot";
export default {
  components:{
    vHead,
    throughAd,
    index,
    vFoot
  }
}
</script>

<style>
#app{
  border-top:2px solid #009a61;
  font-family: -apple-system,"Helvetica Neue",Helvetica,Arial,"PingFang SC","Hiragino Sans GB","WenQuanYi Micro Hei","Microsoft Yahei",sans-serif;
  background-color: #f3f3f3;
}
</style>
