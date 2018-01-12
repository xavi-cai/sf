<template>
  <section class="layer" >
    <div class="layer-zhezhao" @click="hide"></div>
    <div class="layer-con">
       <div>
           <h4>登录</h4>
       </div>
       <div class="clearfix">
            <div class="new">
                111
            </div>
            <div class="login-in">
                登陆
            </div>     
        </div>     
    </div>
  </section>
</template>
<script>
export default {
    data(){
        return {
            layerShow:false
        }
    },
  methods:{
    hide(){
        this.layerShow = !this.layerShow;
    },
    hide(){
        this.$emit('hide',this.layerShow );
    }
  }
}
</script>
<style lang="scss" scoped>
.layer{
    position: relative;
    width: 100%;
    height: 100%;
    .layer-con{
        width: 900px;
        position: fixed;
        left: 50%;
        margin-left: -450px;
        top: 100px;
        background:white;
        z-index: 101;
        border-radius: 0 0 7px 7px;
        text-align: center;
        .clearfix{
            padding: 15px;
        }
        h4{
            text-align: left;
            padding: 15px;
            font-size: 18px;
            background: #f3f3f3;
            border-radius:7px 7px 0 0;
            border-bottom: 1px solid #ccc; 
        }
        .new{
            float: left;
            width: 50%;
        }
        .lonin-in{
            float: left;            
            width: 50%;
        }
    }
    .layer-zhezhao{
        position: fixed;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        background: rgba(0,0,0,.3);
        z-index: 100;
    }

}
</style>
