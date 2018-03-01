<template>
  <div id="leavewords">
    <form id="postMessageForm">
      <input type="text" name="name" placeholder="请输入昵称">
      <input type="text" name="word" placeholder="请输入内容">
      <input type="submit" value="提交">
    </form>
    <div class="text">
      <ul id="messageList">
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    mounted() {
      const appId = "9OjuxqtJW77d99IuXSp1Eug1-gzGzoHsz";
      const appKey = "t9H4TMWKyXzEP2xn2wW1oYzt";
      AV.init({
        appId,
        appKey
      });
      const query = new AV.Query("LeaveWord");
      query.find().then(function(messages) {
        let array = messages.map(item => item.attributes);
        array.forEach(item => {
          let li = document.createElement("li");
          li.innerText = `昵称：${item.name}  
           内容：${item.word}  
           时间：${item.date}`;
          let messageList = document.querySelector("#messageList");
          messageList.appendChild(li);
        });
      });
      let myForm = document.querySelector("#postMessageForm");
      myForm.addEventListener("submit", function(e) {
        e.preventDefault();
        let word = myForm.querySelector("input[name=word]").value;
        let name = myForm.querySelector("input[name=name]").value;
        let date = new Date().toLocaleDateString();
        var TestObject = AV.Object.extend("LeaveWord");
        var message = new TestObject();
        message
          .save({
            date: date,
            word: word,
            name: name
          })
          .then(function(object) {
            let li = document.createElement("li");
            li.innerText = `昵称：${object.attributes.name}  
             内容：${object.attributes.word}  
              时间： ${object.attributes.date}`;
            let messageList = document.querySelector("#messageList");
            messageList.appendChild(li);
            myForm.querySelector("input[name=word]").value = "";
            myForm.querySelector("input[name=name]").value = "";
          });
      });
    }
  };
</script>

<style lang ="scss">
  #leavewords {
    color: #fff;
    display: flex;
    flex-direction: row;
    justify-content: center;

    overflow: hidden;
    >#postMessageForm {
      flex: 1;
      color: #fff;
      margin: 20px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      input:nth-child(1),
      input:nth-child(2) {
        width: 100%;
        color: #fff;
        background: rgba(0,0,0,0.4);
        outline: none;
        font-size: 1em;
        padding: 1em 1em;
        margin-bottom: 2em;
        border: solid 1px #fff;
        -webkit-appearance: none;
      }
      input:nth-child(3) {
        width: 20%;
        outline: none;
        color: #fff;
        padding: .5em 2em;
        margin-top: 12px;
        font-size: 1em;
        -webkit-appearance: none;
        background: #01bcfa;
        border: 1px solid #01bcfa;
        transition: 0.5s all;
        letter-spacing: 1px;
      }
      input:nth-child(3):hover {
        background: none;
        color: #01bcfa;
      }
    }
    >.text {
      /* background: darkcyan; */
      margin: 20px;
      max-height: 300px;
      flex: 1;
      overflow: auto;
      ul {
        >li {
          border-bottom: 1px solid #999;
          padding: 10px;
          color: #fff;
        }
      }
    }
  }
</style>

