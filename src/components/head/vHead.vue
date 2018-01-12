<template>
  <section class="head-top w1110 clearfix">
    <logo></logo>
    <inputbox></inputbox>
    <user-info></user-info>
  </section>
</template>
<script>
import logo from "./children/logo"
import inputbox from "./children/inputbox"
import userInfo from "./children/userInfo"
export default {
  components:{
    logo,
    inputbox,
    userInfo
  }
}
</script>
<style lang="scss" scoped>
 .head-top{
   background: #fafafa;
 }
</style>
