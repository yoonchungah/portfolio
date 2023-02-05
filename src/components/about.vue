<template>
  <div id="About">
    <div class="about_wrap w1440">
      <h2>about me</h2>
      <sction class="about_cont">
        <article class="about_left_wrap mt40">
          <div class="profile_img mt40">
            <img src="../assets/img/profile_img.png" alt="profile_img">
          </div>
          <div class="resume mt40" @click="openResume = true">이력서 확인</div>
          <div class="profile_cont mt40">
            <p>‘왜?’</p>
            이유가 있기 때문에 결과도 있다고 생각합니다.<br>
            항상 의문을 갖고 해답을 찾기 위해 노력하겠습니다.
          </div>
          <div class="profile_icons_wrap mt100">
            <div class="profile_icons hobby_icon" @click="openModalFirst = true">
              <img src="../assets/img/profile_icon1.png" alt="profile_icons">
              <p>취미</p>
            </div>
            <div class="profile_icons personality_icon" @click="openModalLast = true">
              <img src="../assets/img/profile_icon2.png" alt="profile_icons">
              <p>성격</p>
            </div>
          </div>
        </article>
        <article class="about_right_wrap mt40">
          <div class="about_txt_wrap">
            <div class="about_txt mt40">
              <h4 class="about_txt_title">학력</h4>
              <div class="about_txt_cont mt40">
                <p>2018.10 - 2020.01 일본 아카몽카이 어학원 졸업</p>
                <p>2015.03 - 2018.02 인덕대학교 일본어 학과 졸업</p>
                <p>2011.03 - 2014.02 경민 고등학교 졸업</p>
              </div>
            </div>
            <div class="about_txt">
              <h4 class="about_txt_title">수료 내역</h4>
              <div class="about_txt_cont mt40">
                <p>2022.09 - 2023.02 디지털컨버전스 스마트_뷰(Vue)활용 프론트엔드 웹 개발자 양성과정 그린컴퓨터 아카데미 수료 예정</p>
                <p>2020.05 - 2020.09 반응형 ui/ux 웹디자인 그린컴퓨터 아카데미 수료 완료</p>
              </div>
            </div>
            <div class="about_txt">
              <h4 class="about_txt_title">경력 사항</h4>
              <div class="about_txt_cont mt40">
                <p>2020.11 - 2022.05 제이에스벤처스 콘텐츠 기획팀 웹디자이너 근무</p>
                <p>2018.02 평창 동계올림픽 일본 회사 토브톱 투어 인턴 근무</p>
              </div>
            </div>
            <div class="about_txt">
              <h4 class="about_txt_title">자격증</h4>
              <div class="about_txt_cont mt40">
                <p>2022.07 운전면허 2종</p>
                <p>2020.10 GTQ 포토샵 1급</p>
                <p>2020.09 GTQ 일러스트 1급</p>
                <p>2020.02 S-JPT</p>
                <p>2015.06 ITQ MS워드, 파워포인트</p>
              </div>
            </div>
          </div>
        </article>
      </sction>
        <div class="modal_pop" v-if="openModalFirst == true">
          <div class="modal_bg">
            <div class="modal_title">
              <h3>취미</h3>
              <div class="close_btn" @click="openModalFirst = false">
                <span></span>
                <span></span>
              </div>
            </div>
            <div class="modal_img_box">
              <div class="modal_img_box_top">
                <div class="mo_hobby_icon mo_hobby_b"><img src="../assets/img/profile_icon7.png" alt="hobby_icon"></div>
                <div class="mo_hobby_icon mo_hobby_d"><img src="../assets/img/profile_icon8.png" alt="hobby_icon"></div>
                <div class="mo_hobby_icon mo_hobby_m"><img src="../assets/img/profile_icon9.png" alt="hobby_icon"></div>
              </div>
              <div class="modal_img_box_bot">
                <div class="mo_hobby_icon mo_hobby_h"><img src="../assets/img/profile_icon1.png" alt="hobby_icon"></div>
              </div>
            </div>
            <h4 class="modal_cont">
              <p>취미는 독서, 일기 쓰기, 웹툰 보기, 등산이에요 다양한 장르 중에 추리를 좋아하지만 요즘에는 가벼운 장르가 끌려요 가끔씩 일기를 쓰며 생각을 정리하고, 날이 좋을때 등산을 즐겨요</p>
            </h4>
          </div>
        </div>
        <div class="modal_pop" v-if="openModalLast == true">
          <div class="modal_bg">
            <div class="modal_title">
              <h3>성격</h3>
              <div class="close_btn" @click="openModalLast = false">
                <span></span>
                <span></span>
              </div>
            </div>
            <div class="modal_img_box">
              <div class="modal_img_box_top">
                <div class="mo_person_icon mo_person_1"><img src="../assets/img/profile_icon5.png" alt="personality_icon"></div>
                <div class="mo_person_icon mo_person_2"><img src="../assets/img/profile_icon4.png" alt="personality_icon"></div>
                <div class="mo_person_icon mo_person_3"><img src="../assets/img/profile_icon6.png" alt="personality_icon"></div>
              </div>
              <div class="modal_img_box_bot">
                <div class="mo_person_icon mo_person_4"><img src="../assets/img/profile_icon2.png" alt="personality_icon"></div>
              </div>
            </div>
            <h4 class="modal_cont">
              <p>적극적이고 실천력 있어 도전을 망설이지 않아요 좋아하고 관심 있는 것에 끝을 보려는 집착을 갖고 있어요 낯선사람에게 말을 거는게 어렵지 않은 편이에요</p>
            </h4>
          </div>
        </div>
        <!-- 이력서 모달 -->
        <div class="modal_pop_Resume" v-if="openResume == true">
          <div class="modal_Resume_bg">
            <div class="Resume_close_btn" @click="openResume = false">
              <span></span>
              <span></span>
            </div>
            <div class="modal_Resume_img_box">
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
    background-color: #0a0a0a;
    color: #f3f3f3;
  }
  .about_wrap{
    padding-top:8%;
  }
  .about_wrap>h2{
    font-size: 40px;
    text-transform: uppercase;
    font-weight: bold;
  }
  .about_cont{
    display: flex;
    justify-content: space-between;
  }
  /* 왼쪽 */
  .about_left_wrap{
    width: 40%;
  }
  .profile_img{
    width: 100%;
  }
  .resume{
    border: 1px solid #f3f3f3;
    padding: 2%;
    text-align: center;
    width: 200px;
    font-size: 1.125rem;
    cursor: pointer;
    transition: background-color 1s;
    box-sizing: border-box;
  }
  .resume.resume_active{
    background-color: #f3f3f3;
    color: #0a0a0a;
    border: 1px solid #0a0a0a;
    box-sizing: border-box;
  }
  .profile_cont p{
    font-size: 40px;
    padding-bottom: 10px;
  }
  .profile_img img{
    width: 100%;
  }
  .profile_icons_wrap{
    display: flex;
    gap: 10%;
  }
  .profile_icons{
    width: 150px;
    height: 150px;
    border-radius: 100%;
    background-color: #FF6475;
    text-align: center;
    cursor: pointer;
  }
  .profile_icons img{
    width: 70%;
  }
  /* 오른쪽 */
  .about_right_wrap{
    width: 50%;
    border-left: 1px solid #f3f3f3;
  }
  .about_txt_wrap{
    padding-left: 5%;
    box-sizing: border-box;
  }
  .about_txt{
    padding-bottom: 80px;
  }
  .about_txt:last-child{
    padding-bottom: 0;
  }
  .about_txt_title{
    font-size: 1.325rem;
  }
  .about_txt_cont>p{
    margin-bottom: 20px;
  }
  .about_txt_cont>p:last-child{
    margin-bottom: 0;
  }
  /* modal */
  .modal_pop{
    position: fixed;
    top:50%; left: 50%;
    transform: translateX(-50%) translateY(-50%);
    z-index: 99999;
  }
  .modal_bg{
    max-width: 400px;
    box-sizing: border-box;
    background-color: #f3f3f3;
    border-radius: 8px;
    padding-top: 6%;
    padding-bottom: 10%;
    padding-left: 5%;
    padding-right: 5%;
  }
  /* 타이틀과 x버튼 */
  .modal_title{
    font-weight: bold;
    color: #0a0a0a;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .close_btn{
    width: 25px;
    cursor: pointer;
  }
  .close_btn span{
    display: block;
    width: 100%;
    height: 3px;
    background-color: #0a0a0a;
  }
  .close_btn span:nth-child(1){
    display: block;
    transform:rotate(46deg) translate(3px, 5px);
  }
  .close_btn span:nth-child(2){
    margin: 9px 0;
    display: block;
    transform:rotate(312deg) translate(3px, -6px);
  }
  /* 이미지 영역 */
  .modal_img_box{
    width: 100%;
    height: auto;
    border-radius: 8px;
    margin: 20px auto;
    display: flex;
    flex-direction: column;
  }

  /* 취미 */
  .modal_img_box_top{
    display: flex;
    justify-content: space-between;
  }
  .mo_hobby_icon>img{
    width: 90%;
  }
  /* 취미 아이콘 애니메이션 */
  .mo_hobby_b{
    position: relative;
    animation-name: l_r_moving;
    animation-duration: 1s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
    animation-direction: alternate;
  }
  @keyframes l_r_moving {
  0%   {  transform: rotate(-10deg);}
  100%  {  transform: rotate(10deg);}
}

.mo_hobby_d{
    position: relative;
    animation-name: t_b_moving;
    animation-duration: 1s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
    animation-direction: alternate;
  }
  @keyframes t_b_moving {
  0%   {transform:translateY(0);}
  100%  {transform:translateY(-20px);}
  
}

.mo_hobby_m{
    position: relative;
    animation-name: r_l_moving;
    animation-duration: 1s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
    animation-direction: alternate;
  }
  @keyframes r_l_moving {
    0%   {  transform: rotate(10deg);}
  100%  {  transform: rotate(-10deg);}
}


  /* 얼굴 아이콘 */
  .mo_hobby_icon.mo_hobby_h{
    text-align: center;
  }
  .mo_hobby_icon.mo_hobby_h>img{
    width: 70%;
  }
  /* 텍스트 영역 */
  .modal_cont{
    width: 100%;
    margin: 0 auto;
  }
  .modal_cont p{
    color: #0a0a0a;
  }

  /* modal2 */
  .mo_person_icon>img{
    width: 90%;
  }
  /* 성격 아이콘 애니메이션 */
  .mo_person_1{
  position: relative;
  animation-name: person_moving_lr;
  animation-duration: 1s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
  animation-direction: alternate;
  }
  @keyframes person_moving_lr {
    0%   {  transform: rotate(-10deg);}
    100%  {  transform: rotate(10deg);}
  }

.mo_person_2{
    position: relative;
    animation-name: person_moving_tb;
    animation-duration: 1s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
    animation-direction: alternate;
  }
  @keyframes person_moving_tb {
  0%   {transform:translateY(0);}
  100%  {transform:translateY(-20px);}
  
}

.mo_person_3{
    position: relative;
    animation-name: person_moving_rl;
    animation-duration: 1s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
    animation-direction: alternate;
  }
  @keyframes person_moving_rl {
  0%   {  transform: rotate(10deg);}
  100%  {  transform: rotate(-10deg);}
}


  /* 얼굴 아이콘 */
  .mo_person_icon.mo_person_4{
    text-align: center;
  }
  .mo_person_icon.mo_person_4>img{
    width: 70%;
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
    top:3%;
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
    height: 100%;
    background-image: url(../assets/img/chung_resume.png);
    background-repeat: no-repeat;
    background-position: center center;
    background-size: 100% auto;
  }
/* 반응형 */
@media (max-width:1280px){
  .about_wrap>h2{
    font-size: 1.925rem;
  }
  .profile_cont p{
    font-size: 1.925rem;
  }
  .about_txt{
    padding-bottom:3.25rem;
  }
}
@media (max-width:1000px) {
  .about_cont{
    flex-wrap: wrap;
  }
  /* 왼쪽 */
  .about_left_wrap{
    width:100%;
  }
  .resume{
    width: 170px;
  }
    .profile_cont br{
    display: none;
  }
  /* 오른쪽 */
  .about_right_wrap{
    width: 100%;
    border-left: 0;
  }
  .about_txt_wrap{
    padding-left: 0;
  }
}
@media (max-width:800px) {
  .about_wrap>h2{
   font-size: 5.5vw;
 }
 .modal_bg{
  width: 80vw;
 }
 /* 이력서 모달 */
  .modal_pop_Resume{
    padding: 5%;
  }
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
@media (max-width:450px){
  .profile_icons_wrap{
    justify-content: center;
  }
  .profile_icons{
    width: 130px;
    height: 130px;
  }
}
@media (max-width:380px){
  .profile_icons{
    width: 50%;
    height: 50%;
    border-radius: 100%;
  }
}
</style>

<script>
import {onMounted}  from 'vue'
export default {
  name: 'App',

  data() {
    return {
      openModalFirst : false,
      openModalLast : false,
      openResume : false,
    }
  },

  setup(){
      onMounted(() => {
        let resume = document.querySelector('.resume');

        resume.addEventListener('mouseenter',()=>{
          resume.classList.add("resume_active");
          }),

          resume.addEventListener('mouseleave',()=>{
            resume.classList.remove("resume_active");
          })
      })
    }

}
</script>
