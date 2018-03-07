<template>
  <div id="head">
    <div class="name">
      <p></p>
      <h1>苏宋霖</h1>
      <h2>应聘：前端开发工程师</h2>
    </div>
    <div class="contact">
      <h3>联系</h3>
      <h4>
        <a href="mailto:17688877028@163.com">17688877028@163.com</a>
      </h4>
      <h4>+17688877028</h4>
      <h4>25岁/大专/计算机应用</h4>
    </div>
    <div class="blogs">
      <h3>博客</h3>
      <h4><a href="//www.jianshu.com/u/dfe735572ace" target="_blank">简书</a></h4>
      <h4><a href="//github.com/luoshushu" target="_blank">GitHub</a></h4>
      <!-- <h4>GitHub</h4> -->
    </div>
        <div class="blogs">
      <h3>其它</h3>
      <h4>期望城市：广州</h4>
      <h4>期望薪资：税前月薪8k~12k</h4>
      <!-- <h4>GitHub</h4> -->
    </div>
  </div>
</template>
 
<style lang = "scss">
  #head {
    >.name {
      flex-grow: 1;
      >p {
        width: 90px;
        height: 80px;
        background: url(http://oy5vxcq55.bkt.clouddn.com/ssl.png);
        background-size: cover;
        background-repeat: no-repeat;
        background-position: 50% 50%;
        margin-left: auto;
        margin-right: auto;
      }
      >h1 {
        font-size: 22px;
        margin-top: 15px
      }
      >h2 {
        font-size: 16px;
        color: #fff;
              

      }
    }
    >.contact {
      flex-grow: 1;
      >h3 {
        font-size: 28px;
        margin-bottom: 25px;
      }
      >h4 {
        margin-bottom: 15px;
      }
    }
    >.blogs {
      flex-grow: 1;
      >h3 {
        font-size: 28px;
        margin-bottom: 25px;
      }
      >h4 {
        margin-bottom: 30px;
      }
    }
  }
</style>
