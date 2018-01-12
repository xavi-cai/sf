<template>
  <section class="input-box">
      <menu-list></menu-list>
      <div class="v-input">
          <input type="text" placeholder="搜索问题或关键字">
          <button class="fa fa-search"></button>
      </div>
  </section>
</template>
<script>
import menuList from "./menuList"
export default {
  components:{
      menuList
  }
}
</script>
<style lang="scss" scoped>
    .input-box{
        width: 700px;
        position: relative;
        float: left;
        margin-left: 10px;
        .v-input{
            position: absolute;
            right: 15px;
            top: 15px;
            input[type=text]{
                transition: all 0.5s;
                width: 215px;
                border:1px solid #ccc;
                height: 34px;
                padding: 0 36px 0 12px;
                width: 265px;
                border-radius: 5px;                
            }
            input[type=text]::-webkit-input-placeholder{
                color: rgba(153, 153, 153, 0.582);
            }
             input[type=text]:-moz-placeholder{
            color:rgba(153, 153, 153, 0.582);;
                }
            input[type=text]:-ms-input-placeholder{
            color: rgba(153, 153, 153, 0.582);;
                }
            input[type=text]::-moz-placeholder{
            color: rgba(153, 153, 153, 0.582);;
                }
            button{
                position: absolute;
                right: 0;
                top: 0;
                height: 36px;
                width: 36px;
                display: block;
                background: #fff;
                font-size: 20px;
                border: 1px solid #ccc;
                border-left: none;
            }
            button:focus{
                outline: none;
            }
            input[type=text]:focus{
               width: 623px;
               outline: none;
            }
        }
        

    }
</style>