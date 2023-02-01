<template>
  <section id="Intro">
    <article class="intro_wrap w1440">
      <div class="intro_cont">
        <ul class="intro_title">
          <li data-aos="zoom-in-right" data-aos-duration="1800" data-aos-easing="ease-in-out">challenging</li>
          <li data-aos="zoom-in-right" data-aos-duration="1800" data-aos-easing="ease-in-out">logical</li>
          <li data-aos="zoom-in-right" data-aos-duration="1800" data-aos-easing="ease-in-out">analytical</li>
          <li data-aos="zoom-in-right" data-aos-duration="1800" data-aos-easing="ease-in-out">systematic</li>
          <li data-aos="zoom-in-right" data-aos-duration="1800" data-aos-easing="ease-in-out">responsible</li>
        </ul>
        <div class="intro_icon" data-aos="fade-left" data-aos-duration="1800" data-aos-easing="ease-in-out">
          <img src="../assets/img/main_icon.png" alt="icon_me">
        </div>
      </div>
      <div class="intro_sub_title mt40">이유를 찾는<br> 프론트엔드 개발자 윤청아입니다.</div>
    </article>
  </section>
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
  .intro_title li{
    font-size: 74px;
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


@media (max-width:1280px) {
  #Intro{
    height: 100%;
    padding-bottom: 10%;
  }
  .intro_title li{
    font-size: 3.8rem;
  }
  .intro_sub_title{
    font-size: 1.925rem;
  }
}
@media (max-width:800px) {
  .intro_cont{
    flex-direction: column;
  }
  .intro_icon img{
    width: 40%;
  }
  .intro_title li{
    font-size: 10vw;
  }
  .intro_sub_title{
    font-size: 5.5vw;
  }
}
</style>