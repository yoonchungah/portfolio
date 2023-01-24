<template>
  <nav id="main_menu" >
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

  methods : {
    gosection(e){
      //class="gotosce"가 타겟에 없으면 아무것도 하지말고 그냥 리턴 시켜라 중복방지
      if(!e.target.matches(".gotosce")) return;
      e.preventDefault();

      const sec = document.getElementById(e.target.dataset.target);
      if(sec){
        sec.scrollIntoView({behavior : "smooth"});
        }
      },
    },

  }
</script>

<style>
/* 구글 폰트 추가 */
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@100;300;400;500;700;900&display=swap');
#app {
  font-family: 'Noto Sans KR', sans-serif;
  color: #0a0a0a;
}

#main_menu{
  position: fixed;
  top:91%; left: 50%;
  transform: translateX(-50%);
  cursor: pointer;
  width: 1440px;
}
#main_menu.menuFixed{
  position: fixed;
  top:0;
}
#main_menu>ul{
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  margin: 0 auto;
  background-color: #0a0a0a;
  padding-top:2%;
  padding-bottom:2%;
}
#main_menu>ul>li{
  font-weight: bold;
  color: #F3F3F3;
  margin-right: 5%;
}
#main_menu>ul>li:last-child{
  margin-right: 0;
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
