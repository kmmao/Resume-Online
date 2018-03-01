<template>
  <div id="demo">
    <ul>
      <li>
        <a href="//luoshushu.github.io/Carousel/index.html" target="_blank" title="点击查看">
          <img src="//oy5vxcq55.bkt.clouddn.com/demo1.png" alt="">
        </a>
        <p>图片轮播</p>
      </li>
      <li>
        <a href="//luoshushu.github.io/login-and-registration/index.html" target="_blank" title="点击查看">
          <img src="//oy5vxcq55.bkt.clouddn.com/demo2.png" alt="">
        </a>
        <p>登录注册框</p>
      </li>
      <li>
        <a href="//luoshushu.github.io/REM/index.html" target="_blank" title="点击查看">
          <img src="//oy5vxcq55.bkt.clouddn.com/demo3.png" alt="">
        </a>
        <p>动态REM</p>
      </li>
      <li>
        <a href="//luoshushu.github.io/Pikachu/index.html" target="_blank" title="点击查看">
          <img src="//oy5vxcq55.bkt.clouddn.com/demo4.png" alt="">
        </a>
        <p>纯css画皮卡丘</p>
      </li>
      <li>
        <a href="//luoshushu.github.io/Message-board/index.html" target="_blank" title="点击查看">
          <img src="//oy5vxcq55.bkt.clouddn.com/demo5.png" alt="">
        </a>
        <p>留言板</p>
      </li>
      <li>
        <a href="//luoshushu.github.io/Pinterest/index.html" target="_blank" title="点击查看">
          <img src="//oy5vxcq55.bkt.clouddn.com/demo6.png" alt="">
        </a>
        <p>瀑布流照片墙</p>
      </li>
    </ul>
  </div>
</template>

<style lang="scss">
#demo {
  ul {
    display: flex;
    flex-direction: row;
    justify-content: center;
    flex-wrap: wrap;
    > li {
      text-align: center;
      background: #eee;
      width: 300px;
      height: 250px;
      line-height: 30px;
      margin: 24px;
      box-shadow: 0 0px 10px 2px rgba(0, 0, 0, 0.3);
      img {
        width: 100%;
        max-width: 100%;
        height: auto;
        max-height: 190px;
      }
      > p {
        font-size: 16px;
        color: #999;
      }
    }
  }
}
</style>
