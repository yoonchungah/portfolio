<template>
  <div id="About">
    <div class="about_wrap w1440">
      <h2>about me</h2>
      <section class="about_cont">
        <!-- 프로필 이미지 -->
        <article class="about_left_wrap mt40">
          <div class="profile_img">
            <img src="../assets/img/profile_img.png" alt="profile_img">
          </div>
        </article>
        <!-- 간략한 프로필 -->
        <article class="about_right_wrap mt40">
          <div class="about_txt_wrap">
            <h4>도전과 배움을 즐기고 행동에 망설이지 않는 디자이너, <span>윤청아</span></h4>
            <h3 class="mt40">YOONCHUNGAH</h3>
            <ul class="about_info mt40">
              <li><img src="../assets/img/user_icon.png" alt="about_info_img">1996.02.12</li>
              <li><img src="../assets/img/call_icon.png" alt="about_info_img">010 9176 6530</li>
              <li><img src="../assets/img/mail_icon.png" alt="about_info_img">yca3325@gmail.com</li>
              <li><img src="../assets/img/home_icon.png" alt="about_info_img">https://github.com/yoonchungah</li>
            </ul>
            <div class="resume mt40" @click="openResume = true">RESUME</div>
          </div>
        </article>
      </section>

      <!-- 경력 -->
      <section class="work_wrap mt100">
        <p>WORK EXPERIENCE</p>
        <ul class="work_cont mt40">
          <li>2020.11 - 2022.05 제이에스벤처스 콘텐츠 기획팀 웹디자이너 근무</li>
          <li>2018.02 평창 동계올림픽 일본 회사 토브톱 투어 인턴 근무</li>
        </ul>
      </section>
      
      <!-- 공부 -->
      <section class="education_wrap mt100">
        <p>EDUCATION</p>
        <ul class="education_cont mt40">
          <li>2022.09 - 2023.02 디지털컨버전스 스마트_뷰(Vue)활용 프론트엔드 웹 개발자 양성과정 그린컴퓨터 아카데미 수료</li>
          <li>2020.05 - 2020.09 반응형 ui/ux 웹디자인 그린컴퓨터 아카데미 수료</li>
          <li>2018.10 - 2020.01 일본 아카몽카이 어학원 졸업</li>
          <li>2015.03 - 2018.02 인덕대학교 일본어학과 졸업</li>
        </ul>
      </section>

      <!-- 자세 -->
      <section class="mind_wrap mt100">
        <ul class="mind_cont">
          <li class="mind_first" data-aos="fade-up" data-aos-duration="1200" data-aos-easing="ease-in-out">
            <div>
              <img src="../assets/img/mind1.png" alt="mind">
              <h4>#배우려는_자세</h4>
              <p>모르는 것을 부끄러워하지 않고<br>
                하나하나 배워가며 성장하는 것이 즐겁습니다.</p>
            </div>
          </li>
          <li class="mind_second" data-aos="fade-up" data-aos-duration="1200" data-aos-easing="ease-in-out">
            <div>
              <img src="../assets/img/mind2.png" alt="mind">
              <h4>#적응력</h4>
              <p>적응력이 좋아서 새로운 환경에서도<br>
                  융통성 있게 적응할 수 있습니다.</p>
            </div>
          </li>
          <li class="mind_third" data-aos="fade-up" data-aos-duration="1200" data-aos-easing="ease-in-out">
            <div>
              <img src="../assets/img/mind3.png" alt="mind">
              <h4>#책임감</h4>
              <p>목표 지향적이며 맡은 일에 대해<br>
                  책임감을 가지고 수행합니다.</p>
            </div>
          </li>
        </ul>
      </section>
      <!-- 이력서 모달 -->
      <div class="modal_pop_Resume" v-if="openResume == true">
        <div class="modal_Resume_bg">
          <div class="Resume_close_btn" @click="openResume = false">
            <span></span>
            <span></span>
          </div>
          <div class="modal_Resume_img_box">
            <img src="../assets/img/resume.jpg" alt="resume">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
    #About{
      width: 100%;
      height: 100%;
      background-color: #EDEBDF;
    }
    .about_wrap{
      padding-top:8%;
    }
    .about_wrap>h2{
      font-size: 40px;
      text-transform: uppercase;
      font-weight: bold;
    }
    /* 프로필 이미지 */
    .about_cont{
      display: flex;
    }
    .about_left_wrap{
      width: 45%;
      padding-right: 10%;
      box-sizing: border-box;
    }
    .profile_img>img{
      width: 100%;
    }

    /* 간략한 프로필 */
    .about_txt_wrap h4 span{
      color: #203E94;
    }
    .about_txt_wrap h3{
      font-size: 40px;
      font-weight: bold;
      color: #203E94;
    }
    .about_info li{
      padding-bottom:20px;
      font-size: 0.8rem;
    }
    .about_info li:last-child{
      padding-bottom:0px;
    }
    .about_info li img{
      vertical-align: middle;
      margin-right: 3%;
    }
    /* 이력서 */
    .resume{
      background-color: #203E94;
      color: #EDEBDF;
      padding: 2%;
      text-align: center;
      width: 180px;
      cursor: pointer;
      box-sizing: border-box;
    }
     /* 이력서 모달 */
    .modal_pop_Resume{
      position: fixed;
      top:50%; left: 50%;
      transform: translate(-50%, -50%);
      z-index: 99999;
      height: 90vh;
      width: 100%;
      max-width: 800px;
    }
    .modal_Resume_bg{
      box-sizing: border-box;
      padding-top: 5%;
      padding-bottom: 5%;
      padding-left: 5%;
      padding-right: 5%;
      text-align: center;
      width: 100%;
      height: 100%;
      position: relative;
    }
    .Resume_close_btn{
      width: 25px;
      height: auto;
      cursor: pointer;
      z-index: 99999;
      right: 12%;
      top:0;
      position: absolute;
    }
    .Resume_close_btn span{
      display: block;
      width: 100%;
      height: 3px;
      background-color: #0a0a0a;
    }
    .Resume_close_btn span:nth-child(1){
      display: block;
      transform:rotate(46deg) translate(3px, 5px);
    }
    .Resume_close_btn span:nth-child(2){
      margin: 9px 0;
      display: block;
      transform:rotate(312deg) translate(3px, -6px);
    }
    .modal_Resume_img_box{
      position: absolute;
      top:50%; left: 50%;
      transform: translate(-50%, -50%);
      width: 80%;
      /* height: 100%; */
      /* background-color: #fff; */
      /* background-image: url(../assets/img/resume.jpg);
      background-repeat: no-repeat;
      background-position: center center;
      background-size: 100% auto; */
    }
    .modal_Resume_img_box>img{
      width: 100%;
      margin:3%;
      box-sizing: border-box;
    }

    /* 경력 */
    .work_wrap p{
      font-size: 1.125rem;
      font-weight: bold;
    }
    .work_cont li{
      padding-bottom: 20px;
      font-size: 0.8rem;
    }
    .work_cont li:last-child{
      padding-bottom: 0px;
    }

    /* 공부 */
    .education_wrap p{
      font-size: 1.125rem;
      font-weight: bold;
    }
    .education_cont li{
      padding-bottom: 20px;
      font-size: 0.8rem;
    }
    .education_cont li:last-child{
      padding-bottom: 0px;
    }


    /* 자세 */
    .mind_cont{
      display: flex;
      justify-content: space-between;
    }
    .mind_cont li div{
      text-align: center;
    }
    .mind_cont li div h4{
      font-weight: bold;
      padding-top: 20px;
      padding-bottom: 20px;
      font-size: 1.125rem;
    }
    .mind_cont li div p{
      font-size: 0.9rem;
    }
    @media (max-width:1280px){
      .about_wrap>h2{
        font-size: 1.925rem;
      }
      .about_txt_wrap h3{
        font-size: 1.925rem;
      }
      .about_txt{
        padding-bottom:3.25rem;
      }
      /* 자세 */
      .mind_cont li{
        width: 30%;
      }
      .mind_cont li div img{
        width: 30%;
      }
      .mind_cont li div p br{
        display: none;
      }

    }
    @media (max-width:1000px){
      /* 프로필 이미지 */
      .about_cont{
        flex-direction: column;
      }
      .about_left_wrap{
        width: 60%;
        padding-right: 0;
        margin: 0 auto;
      }
      .resume{
        width: 170px;
      }
    }
    @media (max-width:800px) {
      .about_wrap>h2{
        font-size: 5.5vw;
      }
      .about_txt_wrap h3{
        font-size: 5.5vw;
      }
      /* 이력서 모달 */
      .modal_Resume_bg{
        padding-top: 0;
        padding-bottom: 0;
        padding-left: 0;
        padding-right: 0;
      }
      .modal_Resume_img_box{
        background-size: 100% 100%;
      }
    }
</style>

<script>
export default {
  name: 'App',

  data() {
    return {
      openResume : false,
    }
  },

}
</script>