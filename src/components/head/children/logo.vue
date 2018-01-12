<template>
  <section class="logo">
      <h1>
          <a href="#">sf.gg</a>
      </h1>
      <i></i>
  </section>
</template>
<script>
export default {
  
}
</script>
<style lang="scss" scoped>
    .logo{
        float: left;
        text-indent: -999em;
        position: relative;
        h1{
            width: 150px;
            height: 64px;
            background:url(./../../../assets/logo-b.svg) no-repeat center;
            background-size: 100%;
        }       
        h1:hover >::before{
            content: '';
            display: block;
            position: absolute;
            width: 130px;
            height: 100%;
            left: 25px;
            top: 50px;
            z-index: 1;
            background:url(./../../../assets/sf.gg-tip@2x.png) no-repeat;
            background-size:100%;
        }
        i{
            background: url(./../../../assets/hat.svg) no-repeat  center 5px;
            width: 32px;
            height: 20px;
            display: block;
            position: absolute;
            left:30px;
            top: 0;
        }        
    }
    
</style>
