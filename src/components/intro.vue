<template>
  <div id="Intro">
    <div class="intro_wrap w1440">
      <div class="intro_cont">
        <div class="intro_title">
          <p data-aos="fade-right" data-aos-duration="1000" >challenging</p>
          <p data-aos="fade-right" data-aos-duration="1200" >logical</p>
          <p data-aos="fade-right" data-aos-duration="1400" >analytical</p>
          <p data-aos="fade-right" data-aos-duration="1600" >systematic</p>
          <p data-aos="fade-right" data-aos-duration="1800" >responsible</p>
        </div>
        <div class="intro_icon">
          <img src="../assets/img/main_icon.png" alt="icon_me">
        </div>
      </div>
      <div class="intro_sub_title mt40">이유를 찾는 프론트엔드 개발자 윤청아입니다.</div>
    </div>
  </div>
</template>

<script>
import {onMounted}  from 'vue'
  export default{
    setup(){
      onMounted(() => {
        window.addEventListener("scroll",()=>{
          const menu = document.getElementById("main_menu");
          const Intro = document.getElementById("Intro");
          const scrollY = window.pageYOffset;
          if( Intro.offsetTop < scrollY ){
            menu.classList.add('menuFixed');
          } else{
            menu.classList.remove('menuFixed');
          }
        })
      })
  }

};
</script>

<style scoped>
  #Intro{
    width: 100%;
    height: 100vh;
    background-color: #f3f3f3;
  }
  
/* 인트로 내용 */
  .intro_cont{
    display: flex;
    justify-content: space-between;
    padding-top:100px;
  }
  .intro_title p{
    font-size: 72px;
    font-weight: bold;
    text-transform: uppercase;
    color: #FF6475;
  }
  .intro_icon img{
    width: 100%;
  }
  .intro_sub_title{
    font-size: 40px;
    font-weight: bold;
  }
</style>