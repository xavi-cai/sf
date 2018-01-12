<template>
  <section class="user-info">
      <ul class="login-up" @click="show">        
        <li v-for="item in text">{{item.text}}</li>        
      </ul>     
    <tanchu v-if="layerShow" @hide="hide"></tanchu>
  </section>
</template>
<script>

import tanchu from "./tanchu"
export default {
  components:{
    tanchu
  },
  data(){
    return {
      text:[
        {
          text:"免费注册"
        },
        {
          text:"立即能录"
        }
      ],
      layerShow:false
    }
  },
  methods:{
    show(){
      this.layerShow = !this.layerShow;
    },
    hide(msg){
      this.layerShow = msg;
    }

  },
  mounted(){
        this.$on('hide', (data) => {
            if(data){
              console.log(data)
            }
        })
    }
}
</script>
<style lang="scss" scoped>
.user-info{
  float: right;
  width: 250px;
  height: 64px;
  .login-up{
    overflow: hidden;
    padding-top: 15px;
    li{
      float: right;
      width:56px;
      height: 34px;
      padding: 0 13px;
      line-height: 34px;
      margin-left: 15px;
      cursor: pointer;      
      border-radius: 5px;
      font-size: 14px;
    }
    li:hover{
      background: #F3F3F3;
    }
    li:nth-child(2){
      color: #009a61;
    }
    li:nth-child(1){
      color: #fff;
      background-color: #009a61;
      border-color: #008151;
    }
    li:nth-child(1):hover{
      color: #fff;
      background-color: #006741;
      border-color: #00432a;
    }
  }
}
</style>
