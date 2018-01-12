<template>
  <section>
      <div class="foot w1110">
        <ul class="clearfix">
          <li>
            <dl>
              <dt><a href="#">产品</a></dt>
              <dd><a href="#">热门问答</a></dd>
              <dd><a href="#">热门专栏</a></dd>
              <dd><a href="#">热门讲堂</a></dd>
              <dd><a href="#">最新活动</a></dd>
              <dd><a href="#">技术圈</a></dd>
              <dd><a href="#">找工作</a></dd>
              <dd><a href="#">移动客户端</a></dd>
            </dl>
          </li>
          <li>
            <dl>
              <dt><a href="#">资源</a></dt>
              <dd><a href="#">每周精选</a></dd>
              <dd><a href="#">用户排行榜</a></dd>
              <dd><a href="#">徽章</a></dd>
              <dd><a href="#">帮助中心</a></dd>
              <dd><a href="#">声望与权限</a></dd>
              <dd><a href="#">社区服务中心</a></dd>
              <dd><a href="#">开发手册</a></dd>
            </dl>
          </li>
          <li>
            <dl>
              <dt><a href="#">商务</a></dt>
              <dd><a href="#">人才服务</a></dd>
              <dd><a href="#">企业培训</a></dd>
              <dd><a href="#">活动策划</a></dd>
              <dd><a href="#">广告投放</a></dd>
              <dd><a href="#">合作联系</a></dd>
            </dl>
          </li>
          <li>
            <dl>
              <dt><a href="#">关于</a></dt>
              <dd><a href="#">关于我们</a></dd>
              <dd><a href="#">加入我们</a></dd>
              <dd><a href="#">联系我们</a></dd>
            </dl>
          </li>
          <li>
            <dl>
              <dt><a href="#">关注</a></dt>
              <dd><a href="#">产品技术日志</a></dd>
              <dd><a href="#">社区运营日志</a></dd>
              <dd><a href="#">市场运营日志</a></dd>
              <dd><a href="#">团队日志</a></dd>
              <dd><a href="#">社区访谈</a></dd>
              <dd class="spe">
                <a href="#">
                  <i class="fa fa-wechat" style="color:#00b500"></i>
                  <b><img src="./../../assets/appQrcode.png" alt=""><p>扫描关注</p></b>
                </a>
                <a href="#"><i class="fa fa-weibo" style="color:#ec0117"></i></a>
                <a href="#"><i class="fa fa-github" style="color:#3c3c3c"></i></a>
                <a href="#"><i class="fa fa-twitter" style="color:#4baaf4"></i></a>
              </dd>
            </dl>
          </li>
          <li>
            <dl>
              <dt><a href="#">条款</a></dt>
              <dd><a href="#">服务条款</a></dd>
              <dd><a href="#">内容许可</a></dd>
              <dd class="sep1">
                <img src="./../../assets/appQrcode.png" alt="">
              </dd>
              <dd>扫一扫下载APP</dd>
            </dl>
          </li>
        </ul>
      </div>
      <div class="copyright w1110">
        <p>Copyright © 2011-2017 SegmentFault. 当前呈现版本 17.06.16</p>
        <p>
          <a href="#">浙ICP备 15005796号-2</a>
          <a href="#">浙公网安备 33010602002000号</a>
          杭州堆栈科技有限公司版权所有
        </p>
        <p>
         CDN 存储服务由
          <a href="#">又拍云 </a>
           赞助提供 
        </p>
      </div>
  </section>
</template>
<script>
export default {
  
}
</script>
<style lang="scss" scoped>
  .foot{
    padding-top:30px; 
    ul{
      li{
        float: left;
        width: 155px;
        padding: 0 15px;
        dt{
          font-size: 14px;
          font-weight: bold;
          line-height: 25px;
          margin-bottom: 20px;
          a{
            color: #333;
          }
        }
        dd{
          line-height: 26px;
          font-size: 14px;
          a{
            color: #888;
          }
        }
        .spe{
          a{
            margin-right: 5px;
            font-size: 14px;
          }
        }
        .sep1{
          height: 64px;
          width: 64px;
          img{
            width: 100%;
            height: 100%;
          }
        }
        .sep1+dd{
          color: #4baaf4;
        }
      }
    }
    
  }
  .copyright{
      text-align: center;
      p{
        line-height: 30px;
        font-size: 14px;
        color: #4baaf4;
        a{
          color: #888;
          padding: 0 5px;
        }
      }
    }
    // 二维码hover
    .spe>a:nth-child(1){
      position: relative;
    }
    .fa-wechat{
    }
    .spe>a:nth-child(1) b{
      position: absolute!important;
      width: 100px;
      height: 100px;
      display: block;
      left: -52px;
      bottom: 26px;
      background: #fff;
      position: relative; 
      display: none;
      border: 1px solid #ccc;
      box-shadow: 0 5px 10px rgba(0,0,0,0.2);
      padding: 10px;
      img{
        margin: 0 auto;
        width: 88px;
        height: 88px;
        display: block;
      }
      p{
        text-align: center;
        font-size: 12px;
      }

    }
    .spe>a:nth-child(1) b::before{
     border:1px solid;
		    border-color: #fff transparent transparent transparent;
		    left: 50%;
			  overflow: hidden;
		    position: absolute;
		    bottom: -11px;
        margin-left: -10px;
		    width: 0;
		    height: 0;
		    border-width: 6px;
		    border-style: dashed solid dashed dashed;
		    content: '';
    }
    .spe>a:nth-child(1):hover >b{
      display: block;
    }
</style>
