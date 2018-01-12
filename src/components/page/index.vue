<template>
  <section class="con w1110 clearfix">
      <div class="con-left">left</div>
      <div class="con-center">center</div>
      <div class="con-right">right</div>
  </section>
</template>
<script>
export default {
  
}
</script>
<style lang="scss" scoped>
.con{
    margin-top: 30px;
    background: sandybrown;
    >div{
        float: left;
    }
    .con-left{
        width: 160px;
        padding: 0 15px;
    }
    .con-center{
        //  box-sizing:border-box;
         width: 635px;
    }
    .con-right{
        width: 255px;
        padding: 0 15px;
    }
}
</style>
