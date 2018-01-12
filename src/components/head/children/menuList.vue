<template>
    <div>
      <ul class="menu-list clearfix">
        <li v-for="(item,index) in menuList"><a :href="item.url" :class="{point:item.point}"  @mouseover="show(index)"  @mouseout="hide(index)">{{item.text}}</a><i :class="{'fa-caret-down':item.row,fa:item.row}" ></i></li>
           
    </ul>
     <div class="find" style="display:none" v-show="show1" @mouseover="show2()"  @mouseout="show3()">
          <p v-for="item in find" >
            <a :href="item.url">{{item.text}}</a>
            <i v-if="item.hot"  class="fa fa-location-arrow hot" ></i>
            <i v-if="item.hi" class="hi">hi</i>
          </p>
        </div>    
    </div>
</template>
<script>
export default {
  data(){
      return {
        menuList: [
          {
            url:'1111',
            text:'首页',
            point:true,
            row:false
          },
          {
            url:'2222',
            text:'问答',
            point:false,
            row:false
          },
          {
            url:'33333',
            text:'头条',
            point:false,
            row:false
          },
          {
            url:'4444',
            text:'专栏',
            point:false,
            row:false
          },
          {
            url:'5555',
            text:'讲堂',
            point:false,
            row:false
          },
          {
            url:'66666',
            text:'发现',
            point:false,
            row:true
          }
        ],
        find:[
          {
            url:"11111",
            text:"活动",
            hot:false,
            hi:false
          },
          {
            url:"11111",
            text:"技术圈",
            hot:false,
            hi:true
          },
          {
            url:"11111",
            text:"找工作",
            hot:false,
            hi:false
          },
          {
            url:"11111",
            text:"排行榜",
            hot:false,
            hi:false
          },
          {
            url:"11111",
            text:"徽章",
            hot:false,
            hi:false
          },
          {
            url:"11111",
            text:"笔记",
            hot:false,
            hi:false
          },
          {
            url:"11111",
            text:"开发手册",
            hot:true,
            hi:false
          },
          {
            url:"11111",
            text:"广告投放",
            hot:true,
            hi:false
          }
        ] ,
        show1:false,
        timer:''     
    }      
  },
  methods:{
    show(index){
      if(index == 5){
        this.show1 = true;
      }   
    },
    hide(index){    
        if(index == 5){
          console.log()
         this.timer = setTimeout(() => {
            this.show1 = false;
          }, 300);
        }   
    },
    show2(){
      clearTimeout(this.timer);
      this.show1 = true;
    },
    show3(){
      this.show1 = false;
    }
  }
}
</script>
<style lang="scss" scoped>
.menu-list{
  position: relative;
  padding-top: 15px;
  li{
    width: 58px;
    height: 34px;
    float: left;
    line-height: 34px;
    position: relative;
    text-align: center;
    border-radius: 5px;
    a{
      color: #757575;
      font-size: 16px;
      display: block;
      width: 100%;
      height: 100%;
    }
    .point{
      color: #009a61;
      font-weight: 600
    }
    i{
      position: absolute;
      right: 0;
      top: 30%;
    } 
  }
  li:hover{
    background-color: #F3F3F3;
  }
  li:last-child{
    display: block;
  }
}
.find{
    z-index: 99;
    position: absolute;
    left: 288px;
    top: 49px;
    p:nth-last-child(1){
     border-bottom:1px solid #ccc;
     border-radius: 0 0 5px 5px;
    }
    p:nth-child(1){
     border-top:1px solid #ccc;     
     border-radius: 5px 5px 0 0;
    }
    p:hover{
      color: #009a61;
      text-decoration: none;
      background-color: #f3f3f3;
    }
    p{
      border-left:1px solid #ccc;
      border-right:1px solid #ccc;
      width: 94px;
      height: 34px;
      padding: 6px 13px;
      background: #fff;
      position: relative;
      line-height: 34px;
      a{
        color: #757575;
      }
      .hi{
        display: block;
        position: absolute;
        width:18px;
        height: 16px;
        line-height: 16px;
        color: #fff;
        background: red;
        text-align: center;
        border-radius: 40%;
        left: 65px;
        top: 13px;
        font-style: normal;
      
      }
      .hot{
        background: gold;
        color: #fff;
        position: absolute;
        top: 16px;
        right: 30px;
        width: 12px;
        text-align: center;
      }
    }
  }
</style>
