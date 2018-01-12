<template>
    <section class="through-ad" v-if="show">
        <div class="w1110">
            <div>
                AD
            </div>
        </div>
        <i class="fa fa-close close" aria-hidden="true" @click="close"></i>
    </section>
</template>
<script>
export default {
  data(){
      return {
          show:true
      }
  },
  methods:{
      close(){
          this.show = !this.show;
      }
  }
}
</script>
<style lang="scss" scoped>
.through-ad{
    position: relative;
    width: 100%;
    height: 186px;
    background-color:#009a61;
    text-align: center;
    font-size: 50px;
    .close{
        width: 20px;
        height: 20px;
        color: #ccc;
        border: 1px solid #ccc;
        border-radius: 50%;
        display: block;
        position: absolute;
        top: 5px;
        right: 5px;
        font-size: 15px;
        text-align: center;
        line-height: 20px;
        cursor: pointer;
    }
}
</style>
