<template>
  <div id="About">
    <div class="about_wrap w1440">
      <h2>about me</h2>
      <sction class="about_cont">
        <article class="about_left_wrap mt40">
          <div class="profile_img mt40">
            <img src="../assets/img/profile_img.png" alt="profile_img">
          </div>
          <div class="profile_age mt40">1996년생 윤청아</div>
          <div class="profile_cont mt40">
            <p>'왜?'</p>
            이유가 있기 때문에 결과도 있다고 생각합니다.<br>
            항상 의문을 갖고 해답을 찾기 위해 노력하겠습니다.
          </div>
          <div class="profile_icons_wrap mt100">
            <div class="profile_icons hobby_icon">
              <img src="../assets/img/profile_icon1.png" alt="profile_icons">
              <p>취미</p>
            </div>
            <div class="profile_icons personality_icon">
              <img src="../assets/img/profile_icon2.png" alt="profile_icons">
              <p>성격</p>
            </div>
            <div class="profile_icons like_icon">
              <img src="../assets/img/profile_icon3.png" alt="profile_icons">
              <p>취향</p>
            </div>
          </div>

          
        </article>
        <article class="about_right_wrap mt40">
          <div class="about_txt_wrap">
            <div class="about_txt mt40">
              <h4 class="about_txt_title">학력</h4>
              <div class="about_txt_cont mt40">
                <p>2011.03 - 2014.02 경민 고등학교 졸업</p>
                <p>2015.03 - 2018.02 인덕대학교 일본어 학과 졸업</p>
                <p>2018.10 - 2020.01 일본 아카몽카이 어학원 졸업</p>
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
      <!-- 모달창 -->
      <!-- <div class="black-bg" v-if="모달창열렸니 == true">
        <div class="white-bg">
          <h4>제목</h4>
          <p>어쩌구저쩌구웅애웅</p>
        </div>
      </div> -->
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
    padding-top:100px;
    padding-bottom:100px;
  }
  .about_wrap h2{
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
  .profile_cont p{
    font-size: 40px;
  }
  .profile_img img{
    width: 100%;
  }
  .profile_icons_wrap{
    display: flex;
    justify-content: space-between;
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
  .about_txt_cont>p{
    margin-bottom: 20px;
  }
  .about_txt_cont>p:last-child{
    margin-bottom: 0;
  }
  /* modal */
  .black-bg{
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    position: fixed;
    padding: 20px;
  }
  .white-bg{
    width: 100%;
    background-color:#fff;
    border-radius: 8px;
    padding: 20px;
  }
</style>

<!-- <script>
  export default{
    name: 'App',
    data(){
      return{
        //false 닫힘 ture열림
        모달창열렸니 : ture,
      }
    }
  }
</script> -->