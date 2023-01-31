<template>
  <div class="header_wrap">
    <div class="header">
      <div class="ham_nav">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>
  </div>
  <nav id="main_menu">
    <ul>
      <li v-on:click="gosection" data-target="Intro" class="gotosce">INTRO</li>
      <li v-on:click="gosection" data-target="About" class="gotosce">ABOUT ME</li>
      <li v-on:click="gosection" data-target="Skills" class="gotosce">SKILLS</li>
      <li v-on:click="gosection" data-target="Project" class="gotosce">PROJECT</li>
      <li v-on:click="gosection" data-target="Javascript" class="gotosce">JAVASCRIPT</li>
      <li v-on:click="gosection" data-target="Contact" class="gotosce">CONTACT</li>
    </ul>
  </nav>
  <intro />
  <about />
  <skills />
  <project />
  <javascript />
  <contact />
</template>

<script>
import intro from './components/intro.vue';
import about from './components/about.vue';
import skills from './components/skills.vue';
import project from './components/project.vue';
import javascript from './components/javascript.vue';
import contact from './components/contact.vue';


import {onMounted}  from 'vue'
import AOS from 'aos'
import 'aos/dist/aos.css'
export default {
  name: 'App',
  components: {
    intro,
    about,
    skills,
    project,
    javascript,
    contact,

    AOS,

},
  created() {
    AOS.init();
  },
  data() {
    return {
    // menuFixed: "false",
    }
  },
  // methods : {
    
  //   },
    setup(){
      onMounted(() => {
        const menu = document.getElementById("main_menu");
        window.addEventListener("scroll",()=>{
          const scrollY = window.pageYOffset;
          if( Intro.offsetTop < scrollY ){
            menu.classList.add('menuFixed');
          } else{
            menu.classList.remove('menuFixed');
          }
        })

        let header = document.querySelector('.header');
        let span = document.querySelectorAll('span');
        header.addEventListener('click', ()=>{
          menu.classList.toggle('main_nav_active');
          header.classList.toggle('header_active');
          for( let i=0; i<span.length; i++){
            span[i].classList.toggle('span_active');
          }
        });
      })

      function gosection(e){
      if(!e.target.matches(".gotosce")) return;
      e.preventDefault();

      const sec = document.getElementById(e.target.dataset.target);
      if(sec){
        sec.scrollIntoView({behavior : "smooth"});
        }
      }
      
      return{
        gosection,
      }
    }
  }
</script>

<style>
/* 구글 폰트 추가 */
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@100;300;400;500;700;900&display=swap');
#app {
  font-family: 'Noto Sans KR', sans-serif;
  color: #0a0a0a;
}

/* 헤더 */
.header_wrap{
  background-color: #f3f3f3;
  display: none;
}
/* 모바일 네비게이션 */
.ham_nav{
  width: 30px;
  position: fixed;
  top:2%; right: 3%;
  cursor: pointer;
}
.ham_nav span{
  display: block;
  width: 100%;
  height: 3px;
  background-color: #0a0a0a;
  margin: 5px auto;
  transition: all 0.3s ease-in-out;
}
.ham_nav span:nth-child(2){
  transform: translateX(-5px);
}
.ham_nav span:nth-child(3){
  transform: translateX(-10px);
}

/* 햄버거 방향 변경*/
.header_active .ham_nav span:nth-child(2){
  opacity: 0;
}
.header_active .ham_nav span:nth-child(1){
  transform: translateY(8px) rotate(43deg);
}
.header_active .ham_nav span:nth-child(3){
  transform: translateY(-8px) rotate(-43deg);
}

/* 웹 네비게이션 */
#main_menu{
  position: fixed;
  top:calc(100% - 100px); left: 50%;
  transform: translateX(-50%);
  cursor: pointer;
  width: 100%;
  max-width: 1440px;
  transition: top 2s;
  z-index: 9999;
  background-color: #0a0a0a;
  height: 100px;
}
#main_menu.menuFixed{
  position: fixed;
  top:0;
}
#main_menu>ul{
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  height: 100%;
  max-width: 70%;
  margin: 0 auto;
}
#main_menu>ul>li{
  font-weight: bold;
  color: #F3F3F3;
  position: relative;
}
#main_menu>ul>li:hover::after{
  transform: scaleX(1);
}
#main_menu>ul>li::after{
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  height: 3px;
  width: 100%;
  background-color: #FF6475;
  transform: scaleX(0);
  transform-origin: left;
  transition: all .3s;
}

/* 공통 css */
html{
  font-size: 22px;
}
.w1440{
  max-width: 1440px;
  margin: 0 auto;
}
.mt100{
  margin-top: 100px;
}
.mt40{
  margin-top: 40px;
}


/* 미디어 */
@media (max-width:1680px) {
  .w1440{
    max-width: 100%;
    padding-right: 10%;
    padding-left: 10%;
    box-sizing: border-box;
  }
  #main_menu{
    max-width: 90%;
  }
  #main_menu>ul{
    max-width: 80%;
  }
}

@media (max-width:1280px) {
    /* 공통 css */
  html{
    font-size: 18px;
  }
  .mt100{
    margin-top: 60px;
  }
  #main_menu>ul{
    max-width: 100%;
    padding-right: 3%;
    padding-left: 3%;
    box-sizing: border-box;
  }
}
@media (max-width:800px) {
  #main_menu{
    top:0; right: 0;
    transform: translateX(0%);
    max-width: 50%;
    height: 100vh;
    transition: display 2s;
    padding-right: 0;
    padding-left: 0;
    background-color: transparent;
    display: none;
  }
  #main_menu.main_nav_active{
    display: flex;  
  }
  #main_menu.menuFixed{
    position: fixed;
    top:0%;
  }
  #main_menu>ul{
    flex-direction: column;
    max-width: 100%;
    height: 100vh;
    position: absolute;
    top:0; left: 0;
    box-sizing: border-box;
    background-color:#F3F3F3;
    box-shadow: 0px 0px 30px -5px rgba(0,0,0, 0.3);
    padding-top: 70px;
    padding-bottom: 40%;
  }
  #main_menu>ul>li{
    height: 100px;
    color: #0a0a0a;
  }
  #main_menu>ul>li::after{
    top: 30px;
  }
  .header_wrap{
    display: block;
  }

  .ham_nav{
    z-index: 99999;
  }
}
@media (max-width:768px) {
  /* 공통 css */
  html{
    font-size: 16px;
  }
}
@media (max-width:380px) {
  /* 공통 css */
  html{
    font-size: 14px;
  }
}
</style>
