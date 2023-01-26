<template>
  <div id="Skills">
    <div class="skills_wrap w1440">
      <h2>skills</h2>
      <div class="skills_cont mt40">
        <p>저는 이런 것들을 다룰 수 있어요!</p>
        <div class="skills_icons_wrap">
          <div class="skills_icons">
            <div class="skill_box mt40">
              <div class="skill_icon"><img src="../assets/img/icons1.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons2.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons3.png" alt="icon"></div>
            </div>
            <div class="skill_box mt40">
              <div class="skill_icon"><img src="../assets/img/icons4.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons5.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons6.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons7.png" alt="icon"></div>
            </div>
            <div class="skill_box mt40">
              <div class="skill_icon"><img src="../assets/img/icons8.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons9.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons10.png" alt="icon"></div>
            </div>
            <div class="skill_box mt40">
              <div class="skill_icon"><img src="../assets/img/icons11.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons12.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons13.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons14.png" alt="icon"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import {onMounted}  from 'vue'
  export default{
    setup(){
      onMounted(() => {
        window.addEventListener("scroll",()=>{
          const skillBox = document.querySelectorAll('.skill_box');
          for( let i = 0 ; i <skillBox.length; i++){ 
            if( Skills.offsetTop-100 < scrollY ){
              skillBox[i].style.opacity = 1;
              skillBox[i].style.transition = 'all 2s';
              skillBox[i].style.transform = 'scale(0.8)';
            } else{
              skillBox[i].style.opacity = 0;
              skillBox[i].style.transform = 'scale(0.5)';
            }
          }
          
        })
      })
    }
  };
</script>
<style scoped>
  #Skills{
    width: 100%;
    /* height: 100vh; */
    height: 100%;
    background-color: #0A0A0A;
    color: #f3f3f3;
  }
  .skills_wrap{
    padding-top:100px;
    padding-bottom:100px;
  }
  /* title */
  .skills_wrap h2{
    font-size: 40px;
    text-transform: uppercase;
    font-weight: bold;
  }
  .skills_cont>p{
    font-size: 40px;
  }

  /* 아이콘 */
  .skills_icons_wrap{
    width: 100%;
    height: 100%;
  }
  .skill_box{
    display: flex;
    justify-content: space-around;
    opacity: 0;
    transform: scale(0.5);
  }
</style>






