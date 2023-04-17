<template>
  <section id="Intro">
    <article class="intro_wrap w1440">
      <div class="intro_cont">
        <ul class="intro_title">
          <li data-aos="fade-right" data-aos-duration="1200" data-aos-easing="ease-in-out">challenging</li>
          <li data-aos="fade-right" data-aos-duration="1600" data-aos-easing="ease-in-out">logical</li>
          <li data-aos="fade-right" data-aos-duration="2000" data-aos-easing="ease-in-out">analytical</li>
          <li data-aos="fade-right" data-aos-duration="2400" data-aos-easing="ease-in-out">systematic</li>
          <li data-aos="fade-right" data-aos-duration="2800" data-aos-easing="ease-in-out">responsible</li>
        </ul>
      </div>
      <div class="intro_sub_title mt40">안녕하세요. 항상 ‘의문을 갖고 해답을 찾기 위해 노력하자’ 라는 마음으로 공부하고 있습니다.<br>
천리길도 한걸음부터라는 말처럼 꾸준히 포기하지 않고 나아가겠습니다.</div>
    </article>
  </section>
</template>



<style scoped>
  #Intro{
    width: 100%;
    height: 100vh;
    background-color: #EDEBDF;
    box-sizing: border-box;
  }

/* 인트로 내용 */
  .intro_cont{
    padding-top:40px;
  }
  .intro_title li{
    font-size: 80px;
    font-weight: bold;
    text-transform: uppercase;
    color: #203E94;
  }
  .intro_sub_title{
    font-size: 18px;
  }


@media (max-width:1280px) {
  #Intro{
    padding-bottom: 10%;
  }
  .intro_title li{
    font-size: 4rem;
  }
  .intro_sub_title{
    font-size: 2vw;
  }
}
@media (max-width:800px) {
  #Intro{
    height: 100%; 
  }
  .intro_title li{
    font-size: 10vw;
  }
  .intro_sub_title{
    font-size: 3vw;
  }
}
</style>