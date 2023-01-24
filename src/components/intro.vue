<template>
  <div id="Intro">
    <div class="header_wrap">
      <div class="header">
        <div class="header_title"><h2>chungah Portfolio</h2></div>
        <div class="ham_nav">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
    </div>
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
          <img src="../../public/img/main_icon.png" alt="icon_me">
        </div>
      </div>
      <div class="intro_sub_title mt40">이유를 찾는 프론트앤드 개발자 윤청아입니다.</div>
    </div>
  </div>
</template>

<script>
  export default{

  };
</script>

<style scoped>
  #Intro{
    width: 100%;
    height: 100vh;
    background-color: #f3f3f3;
  }
  /* 헤더 */
  .header{
    padding: 40px 3%;
    box-sizing: border-box;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .header_title h2{
    font-weight: bold;
    text-transform: uppercase;
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

/* 인트로 내용 */
  .intro_cont{
    display: flex;
    justify-content: space-between;
  }
  .intro_title p{
    font-size: 72px;
    font-weight: bold;
    text-transform: uppercase;
    color: #FF6475;
  }
  .intro_sub_title{
    font-size: 40px;
    font-weight: bold;
  }
</style>