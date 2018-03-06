<template>
  <div id="content">
    <h2>项目经历</h2>
    <nav>
      <ol>
        <li v-bind:class="{active: currentTab === 0}" v-on:click="currentTab = 0 ">PROJECT </li>
        <li v-bind:class="{active: currentTab === 1}" v-on:click="currentTab = 1 ">DEMO</li>
      </ol>
    </nav>
    <ol class="write">
      <li v-bind:class="{active: currentTab === 0}">
        <Items/>
      </li>
      <li v-bind:class="{active: currentTab === 1}">
        <Demo/>
      </li>
    </ol>
    <div class="about">
      <Skill class="skill" />
      <Work class="work" />
    </div>
    <div class="download">
      <h2>下载我的简历</h2>
      <a href="http://p55bxl1en.bkt.clouddn.com/%E5%BA%94%E8%81%98%E5%89%8D%E7%AB%AF%E5%B7%A5%E7%A8%8B%E5%B8%88-%E8%8B%8F%E5%AE%8B%E9%9C%96-17688877028.pdf" download title="点击下载我的简历">Download</a>
    </div>
  </div>
</template>

<script>
  import Items from "./Items";
  import Demo from "./Demo";
  import Skill from "./Skill";
  import Work from "./Work";
  export default {
    components: {
      Items,
      Demo,
      Skill,
      Work
    },
    data() {
      return {
        currentTab: 0
      }
    }
  }
</script>
 
<style lang = "scss">
  #content {
    display: flex;
    flex-direction: column;
    >.about {
      display: flex;
      justify-content: center;
      background: #212121;
    }
    .download {
      text-align: center;
      min-height: 200px;
      h2 {
        font-size: 36px;
        padding: 32px 0;
      }
      >a {
        font-size: 2em;
        padding: 5px 10px;
        color: #fff;
        background: #01bcfa;
        transition: 0.5s all;
      }
      a:hover {
        color: #000;
      }
    }
    >h2 {
      font-size: 36px;
      padding-top: 32px;
    }
    nav {
      margin: 0 64px;
      >ol {
        display: flex;
        flex-direction: row;
        justify-content: center;
        border-bottom: 1px solid #eee;
        margin: 32px 0;
        >li {
          font-size: 16px;
          text-align: center;
          margin: 0 32px;
          cursor: pointer;
          transition: 0.5s all;
          border-bottom: 2px solid transparent;
        }
        & .active {
          border-bottom: 2px solid #00c5b5;
          color: #00c5b5;
        }
        li:hover {
          border-color: #00c5b5;
          color: #00c5b5;
        }
      }
    }
    >.write {
      overflow: hidden;
      flex: 1;
      margin: 32px;
      >li {
        display: none;
        height: 100%;
      }
      & .active {
        display: block;
      }
    }
  }
</style>


