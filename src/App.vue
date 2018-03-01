<template>
  <div id="app">
    <Head class="head" />
    <Content class="content" />
    <Rump class="rump" />
  </div>
</template>

<script>
  import Head from "./components/Head";
  import Content from "./components/Content";
  import Rump from "./components/Rump";
  export default {
    name: "App",
    components: {
      Head,
      Content,
      Rump
    }
  };
</script>

<style lang="scss">
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Merriweather Sans', sans-serif;
  }
  a {
    text-decoration: none;
    color: #fff;
    transition: 1s all;
  }
  a:hover {
    color: #00bcd4;
  }
  h1,
  h2,
  h3,
  h4,
  h5,
  h6 {
    text-align: center;
    font-family: "Roboto", sans-serif;
    letter-spacing: 1px;
  }
  h2 {
    color: #00bcd4;
  }
  li {
    list-style: none;
  }
  #app {
    display: flex;
    flex-direction: column;
    font-family: 'Merriweather Sans', sans-serif;
    >.head {
      background: url(http://oy5vxcq55.bkt.clouddn.com/beijing.jpg);
      background-size: cover;
      background-repeat: no-repeat;
      background-position: 50% 50%;
      color: #fff;
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;
      height: 350px;
      position: relative;
      z-index: 1;
    }
    >.head::before {
      content: ' ';
      display: block;
      background: rgba(0, 0, 0, 0.2);
      position: absolute;
      top: 0;
      left: 0;
      bottom: 0;
      right: 0;
      z-index: -1;
    }
    >.rump {
      overflow: hidden;
      background: url(http://oy5vxcq55.bkt.clouddn.com/bottom.jpg);
      background-size: cover;
      background-repeat: no-repeat;
      background-position: 50% 50%;
      min-height: 400px;
    }
  }
</style>
