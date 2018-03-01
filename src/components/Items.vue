<template>
  <div id="items">
    <ul>
      <li>
        <div class="show">
          <img src="//oy5vxcq55.bkt.clouddn.com/project1.png" alt="">
          <p>在线简历编辑器<a href="https://github.com/luoshushu/vue-resume" target="_blank" title="点击查看源码">源码</a><a href="https://luoshushu.github.io/vue-resume/dist/index.html" target="_blank" title="点击预览效果">预览</a></p>
        </div>
        <div class="text">
          <div class="intro">
            <h2>功能介绍</h2>
            <p>
              在线简历编辑、预览
            </p>
          </div>
          <div class="intro">
            <h2>技术细节</h2>
            <p>
              预览按钮： 原理当点击预览按钮时，把头部、左边的这两个区域的内容给隐藏就可以了 display: none。 当点退出预览时，即 display: block.
              <a href="//www.jianshu.com/p/6f695b5f3740" target="_blank">阅读全文</a>
            </p>
          </div>
          <div class="intro">
            <h2>技术栈</h2>
            <p>
              webpack ----打包神器
            </p>
            <p>
              vue-cli ----快速构建项目
            </p>
            <p>
              scss ----方便的css
            </p>
            <p>
              element-ui ---- UI组件库
            </p>
            <p>
              normalize.css ---- 重置掉该重置的样式
            </p>
          </div>
        </div>
      </li>
      <li>
        <div class="show">
          <img src="//oy5vxcq55.bkt.clouddn.com/project2.png" alt="">
          <p>豆瓣电影<a href="https://github.com/luoshushu/douban" target="_blank" title="点击查看源码">源码</a><a href="https://luoshushu.github.io/douban/index.html" target="_blank" title="点击预览效果">预览</a></p>
        </div>
        <div class="text">
          <div class="intro">
            <h2>功能介绍</h2>
            <p>
              豆瓣电影top250排名，以及北美票房榜，搜索功能等
            </p>
          </div>
          <div class="intro">
            <h2>技术细节</h2>
            <p>
              问题：如何判断滚动到底部？ 页面面板总长度 = 视窗高度 + 滚动高度 页面面板总长度 ： $('section').eq(0).height() 视窗高度 ：$('main').height() 滚动高度 ：$('main').scrollTop()
              <a href="//www.jianshu.com/p/728cf113a662" target="_blank">阅读全文</a>
            </p>
          </div>
          <div class="intro">
            <h2>技术栈</h2>
            <p>
              运用jQuery开发操作，ajax实现数据交互，豆瓣API,RequireJS，对象等模块化开发
            </p>
          </div>
        </div>
      </li>
      <li>
        <div class="show">
          <img src="//oy5vxcq55.bkt.clouddn.com/project3.png" alt="">
          <p>pc端在线音乐FM<a href="https://github.com/luoshushu/MusicFm" target="_blank" title="点击查看源码">源码</a><a href="https://luoshushu.github.io/MusicFm/index.html" target="_blank" title="点击预览效果">预览</a></p>
        </div>
        <div class="text">
          <div class="intro">
            <h2>功能介绍</h2>
            <p>
              音乐的播放、暂停、音量大小调节、歌词显示、音乐分类、点击进度条实现相应的播放时段
            </p>
          </div>
          <div class="intro">
            <h2>技术细节</h2>
            <p>
              音乐分类左右滚动按钮: 当点击左/右按钮，让当前ul做 一个移动，移动当前ul的宽度 li的个数 = Math.floor（list容器的宽度/当前每一个li的宽度） left = li的个数*当前每一个li的宽度
              <a href="//www.jianshu.com/p/eb31c0fd953c" target="_blank">阅读全文</a>
            </p>
          </div>
          <div class="intro">
            <h2>技术栈</h2>
            <p>
              运用jQuery开发操作，ajax实现数据交互，百度音乐的API，webpack构建工具进行打包压缩
            </p>
          </div>
        </div>
      </li>
      <li>
        <div class="show">
          <img src="//oy5vxcq55.bkt.clouddn.com/project4.png" alt="">
          <p>微信小程序天气预报<a href="//github.com/luoshushu/weixin-weather" target="_blank" title="点击查看源码">源码</a><a href="http://oy5vxcq55.bkt.clouddn.com/weather.jpg" target="_blank" title="点击预览效果">预览</a></p>
        </div>
        <div class="text">
          <div class="intro">
            <h2>功能介绍</h2>
            <p>
              今日天气情况，近期10天的天气情况
            </p>
          </div>
          <div class="intro">
            <h2>技术细节</h2>
            <p>
            </p>
          </div>
          <div class="intro">
            <h2>技术栈</h2>
            <p>
              JavaScript+WXML+WXSS
            </p>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<style lang = "scss">
  #items {
    ul {
      display: flex;
      flex-direction: column;
      flex-wrap: wrap;
      text-align: center;
      >li:nth-child(odd) {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
      }
      >li {
        height: 300px;
        margin: 40px 30px;
        padding-bottom: 50px;
        display: flex;
        flex-direction: row-reverse;
        justify-content: space-between;
        border-bottom: 1px solid #ddd;
        >.text {
          display: flex;
          padding: 0 40px;
          >.intro {
            width: 200px;
            padding: 0 5px;
            border-right: 1px dotted #00bcd4;
            overflow: hidden;
            >h2 {
              color: #fdac14;
              font-size: 1.5em;
            }
            >p {
              line-height: 1.5em;
              font-size: 14px;
              margin: 1em 0;
              color: #999;
              overflow: hidden;
              a {
                color: #fdac14;
              }
            }
          }
          .intro:nth-child(1) {
            border-left: 1px dotted #00bcd4;
          }
        }
        .show {
          position: relative;
          box-shadow: 0 0px 10px 2px rgba(0, 0, 0, 0.3);
          /* width: 380px; */
          max-width: 380px;
          flex-grow: 1;
          img {
            min-width: 380px;
            max-width: 380px;
            width: 100%;
            height: 100%;
          }
          p {
            color: #999;
            padding-top: 15px;
            font-size: 16px;
            >a {
              font-size: 12px;
              color: #F69027;
              border: 1px solid #F69027;
              padding: 0 10px;
              border-radius: 10px;
              margin: 5px;
            }
            >a:hover {
              background: #ddd;
              /* color: #fff; */
            }
          }
        }
      
      }
    }
  }
</style>
