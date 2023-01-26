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
        window.addEventListener("scroll",()=>{
          const menu = document.getElementById("main_menu");
          const scrollY = window.pageYOffset;
          if( Intro.offsetTop < scrollY ){
            menu.classList.add('menuFixed');
          } else{
            menu.classList.remove('menuFixed');
          }
        })
      })

      function gosection(e){
      //class="gotosce"가 타겟에 없으면 아무것도 하지말고 그냥 리턴 시켜라 중복방지
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
.ham_nav{
  width: 30px;
  position: fixed;
  top:5%; right: 3%;
}
.ham_nav span{
  display: block;
  width: 100%;
  height: 3px;
  background-color: #0a0a0a;
}
.ham_nav span:nth-child(2){
  margin: 5px 0;
  transform: translateX(-5px);
}
.ham_nav span:nth-child(3){
  transform: translateX(-10px);
}

/* 네비게이션 */
#main_menu{
  position: fixed;
  top:calc(100% - 100px); left: 50%;
  transform: translateX(-50%);
  cursor: pointer;
  width: 1440px;
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
  background: #FF6475;
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

</style>
