<template>
  <section id="Javascript">
    <article class="script_wrap w1440">
     <h2>toy project</h2>
     <nav class="jscript_box mt40">
       <ul class="jscript mt40">
         <li class="toypj">
          <div class="todolist">
            <a href="http://toys96.dothome.co.kr/toy1/index.html" target="_blank"></a>
          </div>
          <p>스케줄을 관리해주는 TO DO LIST입니다.
              할 일을 추가하고, 체크하고 삭제할 수 있습니다.
              bootstrap 라이브러리를 활용하여 반응형 작업을 손쉽게 마쳤습니다.
          </p>
         </li>
         <li class="toypj">
          <div class="randomgame">
            <a href="http://toys96.dothome.co.kr/toy2/index.html" target="_blank"></a>
          </div>
          <p>숫자맞추기 게임입니다. 랜덤함수를 이용하였으며,
              1부터 100가지의 숫자중 정답을 맞추는 게임입니다.
              총 7번의 기회가 주어지며 개발자모드로 정답을 확인할 수 있습니다.
              리셋 기능을 추가하여 게임을 반복해서 할 수 있도록 구현했습니다.</p>
         </li>
         <li class="toypj">
          <div class="shootinggame">
            <a href="http://toys96.dothome.co.kr/toy3/index.html" target="_blank"></a>
          </div>
          <p>슈팅게임입니다. 자바스크립트의 캔버스 함수를 이용하여 
              별도의 css 작업 없이 이미지를 구현한 게임입니다.
              방향키를 이용하여 우주선을 움직일 수 있으며, 스페이스바로 총알을
              생성하여 적을 무찌를 수 있습니다.</p>
         </li>
         <li class="toypj">
          <div class="dosirak">
            <a href="http://cloning96.dothome.co.kr/dosirak_cloning/index.html" target="_blank"></a>
          </div>
          <p>도시락통 사이트를 사이트를 웹접근성과 마크업에 중점을 두고 클론코딩한 반응형 사이트입니다.
              스와이퍼 라이브러리를 이용하여 웹버전과 모바일 버전의 배너를 구현 했습니다.
              자바스크립트로 클래스명을 추가하는 방법을 사용하여 스크롤시 네비게이션이 변화하도록 구현 했습니다.
              또 마우스 오버시 색상이 변화하는 효과를 주었습니다.</p>
         </li>
         <li class="toypj">
          <div class="shouse">
            <a href="http://cloning96.dothome.co.kr/shouse_cloning/index.html" target="_blank"></a>
          </div>
          <p>싱그러운 집 사이트를 웹접근성과 마크업에 중점을 두고 클론코딩한 반응형 사이트입니다.
                스와이퍼 라이브러리를 이용하여 웹버전과 모바일 버전의 배너를 구현 했습니다.</p>
         </li>
         <li class="toypj">
          <div class="richmond">
            <a href="http://cloning96.dothome.co.kr/richmond_cloning/index1.html" target="_blank"></a>
          </div>
          <p>더리치몬드 평창사이트를 웹접근성과 마크업에 중점을 두고 클론코딩한 반응형 사이트입니다.
              비디오태그를 사용하여 영상이 자동재생되도록 했으며, 자바스크립트를 이용하여 서브메뉴를 구현했습니다.
              또 이벤트리스너를 활용하여 마우스 오버시 이미지가 변화하는 효과를 주었습니다.</p>
         </li>
       </ul>
     </nav>
    </article>
  </section>
 </template>
 <style scoped>
  #Javascript{
  width: 100%;
  height: 100%;
  background-color: #EDEBDF;
 }
 .script_wrap{
   padding-top:8%;
   padding-bottom:8%;
 }
 /* title */
 .script_wrap>h2{
   font-size: 40px;
   text-transform: uppercase;
   font-weight: bold;
 }
 /* 리스트 */
 .jscript{
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  /* gap: 3%; */
 }
 .toypj{
  width: 30%;
  text-align: center;
 }
 .toypj>div{
  width: 350px;
  height: 350px;
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  margin: 0 auto;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;
  transition: scale 1s;
 }
 .toypj>div:hover{
  scale: 1.1;
 }
 .todolist{
  background-image: url(../assets/img/mockup_img01.png);
 }
 .randomgame{
  background-image: url(../assets/img/mockup_img02.png);
 }
 .shootinggame{
  background-image: url(../assets/img/mockup_img03.png);
 }
 .dosirak{
  background-image: url(../assets/img/mockup_img04.png);
 }
 .shouse{
  background-image: url(../assets/img/mockup_img05.png);
 }
 .richmond{
  background-image: url(../assets/img/mockup_img06.png);
 }
 .toypj a{
  width: 100%;
  height: 100%;
  display: block;
 }
 .toypj p{
  font-size: 0.8rem;
  padding-top: 20px;
  padding-bottom:100px;
  padding-left: 3%;
  padding-right: 3%;
  box-sizing: border-box;
  text-align: left;
 }
 @media (max-width:1280px) {
  .script_wrap>h2{
    font-size: 1.925rem;
  }
  .toypj>div{
    width: 25vw;
    height: 25vw;
  }
 }
 @media (max-width:800px) {
  .script_wrap>h2{
    font-size: 5.5vw;
  }
  .toypj{
    width: 50%;
  }
   .toypj>div{
    width: 35vw;
    height: 35vw;
  }
  .toypj p{
  padding-bottom:50px;
 }
}
@media (max-width:600px){
  .toypj{
    width: 100%;
  }
  .toypj>div{
    width: 40vw;
    height: 40vw;
  }
}
 </style>