<template>
  <div id="Intro">
    <div class="intro_wrap w1440">
      <div class="intro_cont">
        <div class="intro_title">
          <span data-aos="fade-right" data-aos-duration="1000" >challenging</span>
          <span data-aos="fade-right" data-aos-duration="1200" >logical</span>
          <span data-aos="fade-right" data-aos-duration="1400" >analytical</span>
          <span data-aos="fade-right" data-aos-duration="1600" >systematic</span>
          <span data-aos="fade-right" data-aos-duration="1800" >responsible</span>
        </div>
        <div class="intro_icon">
          <img src="../assets/img/main_icon.png" alt="icon_me">
        </div>
      </div>
      <div class="intro_sub_title mt40">이유를 찾는 프론트엔드 개발자 윤청아입니다.</div>
    </div>
  </div>
</template>



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
    padding-top:40px;
  }
  .intro_title{
    display: flex;
    flex-direction: column;
  }
  .intro_title span{
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