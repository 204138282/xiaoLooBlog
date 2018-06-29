<template>
  <!-- Header -->
  <div class="base">
    <div id="header">
      <!-- <img class="avatar" src="../../assets/logo.png"> -->
      
      <div class="logo-title">
        <div style="height: 2px; background-color: #000; width: 150px;"></div>
        <span class="span">{{ msg }}</span>  
        <div style="height: 2px; background-color: #000; width: 150px;"></div>
      </div>
      <nav>
        <ul class="main">
          <li>
            <a href="#">Home</a>
            <ul class="drop menu6">
              <li><a href="#">工作</a></li>
              <li><a href="#">生活</a></li>
              <li><a href="#">学习</a></li>
              <li><a href="#">休闲</a></li>
            </ul>
          </li>
          <li><a href="#">Play</a>
            <ul class="drop menu6">
              <li><a href="#">games</a></li>
              <li><a href="#">music</a></li>
              <li><a href="#">videos</a></li>
            </ul>
          </li>
          <li><a href="#">Profile</a>
            <!-- <ul class="drop menu6">
              <li><a href="#">Home</a></li>
              <li><a href="#">news</a></li>
              <li><a href="#">contact</a></li>
              <li><a href="#">about</a></li>
            </ul> -->
          </li>
          <li><a href="#">Work</a>
            <ul class="drop menu6">
              <li><a href="#">听听</a></li>
              <li><a href="#">说说</a></li>
              <li><a href="#">看看</a></li>
            </ul>
          </li>
          <li><a href="#">Team</a>
            <ul class="drop menu6">
              <li><a href="#">团队项目</a></li>
              <li><a href="#">团队计划</a></li>
            </ul>
          </li>
          <li><a href="#">about</a>
            <ul class="drop menu6">
              <li><a href="#">简介</a></li>
              <li><a href="#">自传</a></li>
            </ul>
          </li>
        </ul>
      </nav>
<!--       <div class="menu" id="menu" @click="clickMenu">
        <span class="line line1"></span>
        <span class="line line2"></span>
        <span class="line line3"></span>
      </div> -->
    </div>
    <body>
      <div class="content">
        <p>相隔上一次的更新我掰手指数一数，下意识的双腿一软，给各位小哥哥小姐姐们跪下了。自从有了对象后，周末几乎落下了主题的进度（邪魅的笑）。一边开发新的主题，一边收集您们给我反馈回来的"臭虫"，还有新的主题后台看见了些大神在... </p>
        <p>相隔上一次的更新我掰手指数一数，下意识的双腿一软，给各位小哥哥小姐姐们跪下了。自从有了对象后，周末几乎落下了主题的进度（邪魅的笑）。一边开发新的主题，一边收集您们给我反馈回来的"臭虫"，还有新的主题后台看见了一些大神在... </p>
      </div>  
    </body>
  </div>
</template>

<!-- Scripts -->
<script>      
  export default {
    name: 'home',
    data () {
      return {
        msg: 'No zero , be one .'
      }
    },
    created() {
      this.$loading.show('正在加载中...(此提示将在5秒后消失!)')
      setTimeout(() => {
        this.$loading.hide()
      }, 5000);
    },
    methods: {
      clickMenu:function () {
        console.log('123')
      }
    }
  }
</script>


<style scoped>
@import '../../resource/css/style.css';

/*.base {
  width: 100%;
  position: absolute;
  top: 0;
  background-image: url(../../assets/bg-veer.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  margin-left: -10px;
  }*/

  #header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }

  .avatar {
    width: 60px;
    height: 60px;
    border-radius: 50%;
    margin-left: 1em;
  }

  .logo-title {
    display: flex;
    margin-left: 50px;
    flex-direction: column;
    align-items: center;
  }

  .span {
    color: #000;
    font-size: 26px;
    font-weight: 600;
  }

  .menu {
    display: block;
    position: absolute;
    z-index: 999;
    top: 2em;
    right: 3em;
    width: 36px;
    height: 36px;
    cursor: pointer;
    -webkit-transition: all 0.3s ease-in-out;
    -o-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
  }
  .line {
    width: 40px;
    height: 2px;
    display: block;
  }
  .line1 {
    top: 0px;
    background: rgba(255, 255, 255, 1);
  }
  .line2 {
    margin-top: 12px;
    background: rgba(255, 255, 255, 1);
  }
  .line3 {
    margin-top: 12px;
    background: rgba(255, 255, 255, 1);
  }

  .content {
    margin: 10px 20px;
  }

  #menu:before{
    content: "";
    position: absolute;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
    width: 70px;
    height: 70px;
    border: 5px solid rgba(0, 0, 0, 0);
    top: calc(50% - 35px);
    left: calc(50% - 35px);
    border-radius: 100%;
    -webkit-transition: all 0.3s ease-in-out;
    -o-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
  }

  #menu.is-active:before{
    border: 5px solid #ecf0f1;
  }

  #menu.is-active .line{
    width: 35px;
  }

  #menu.is-active .line:nth-child(2){
    opacity: 0;
  }

  #menu.is-active .line:nth-child(1){
    -webkit-transform: translateY(13px);
    -ms-transform: translateY(13px);
    -o-transform: translateY(13px);
    transform: translateY(13px);
  }

  #menu.is-active .line:nth-child(3){
    -webkit-transform: translateY(-13px) rotate(90deg);
    -ms-transform: translateY(-13px) rotate(90deg);
    -o-transform: translateY(-13px) rotate(90deg);
    transform: translateY(-13px) rotate(90deg);
  }


</style>
