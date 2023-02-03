<template>
  <section id="Skills">
    <article class="skills_wrap w1440">
      <h2>skills</h2>
      <div class="skills_cont mt40">
        <p>저는 이런 것들을 다룰 수 있어요!</p>
        <div class="skills_icons_wrap">
          <ul class="skills_icons">
            <li class="skill_box mt40">
              <div class="skill_icon"><img src="../assets/img/icons5.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons9.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons3.png" alt="icon"></div>
            </li>
            <li class="skill_box mt40">
              <div class="skill_icon"><img src="../assets/img/icons6.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons10.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons11.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons1.png" alt="icon"></div>
            </li>
            <li class="skill_box mt40">
              <div class="skill_icon"><img src="../assets/img/icons7.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons12.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons2.png" alt="icon"></div>
            </li>
            <li class="skill_box mt40">
              <div class="skill_icon"><img src="../assets/img/icons8.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons13.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons14.png" alt="icon"></div>
              <div class="skill_icon"><img src="../assets/img/icons4.png" alt="icon"></div>
            </li>
          </ul>
        </div>
      </div>
    </article>
  </section>
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
              skillBox[i].classList.add("skill_active");
            } else{
              skillBox[i].classList.remove("skill_active");
            }
          }
          
        })

        const skillIcon = document.querySelectorAll('.skill_icon');
        for(let j=0; j<skillIcon.length; j++){
          skillIcon[j].addEventListener('mouseenter',()=>{
            skillIcon[j].classList.add("skill_icon_active");
          }),
          skillIcon[j].addEventListener('mouseleave',()=>{
            skillIcon[j].classList.remove("skill_icon_active");
          })
        }

      })
    }
  };
</script>
<style scoped>
  #Skills{
    width: 100%;
    height: 100%;
    background-color: #0A0A0A;
    color: #f3f3f3;
  }
  .skills_wrap{
    padding-top:8%;
    padding-bottom:8%;
  }
  /* title */
  .skills_wrap>h2{
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
    cursor: pointer;
    transition: all 2s;
    text-align: center;
  }
  .skill_box.skill_active{
    opacity: 1;
    transition: all 2s;
  }
  .skill_icon{
    transition: all 1s;
    text-align: center;
  }
  .skill_icon img{
    width: 80%;
  }
  .skill_icon.skill_icon_active{
    transform: scale(1.3);
  }

  @media (max-width:1280px){
    /* title */
    .skills_wrap>h2{
      font-size: 1.925rem;
    }
  }
  @media (max-width:800px){
    /* title */
    .skills_wrap>h2{
      font-size: 5.5vw;
    }
    .skills_cont>p{
      display: none;
    }
    .skill_box{
      justify-content: space-between;
    }

    .skill_icon{
      transform: none;
    }
    .skills_icons{
      width: 100%;
      height: 100%;
    }
    .skill_icon.skill_icon_active{
      transform: none;
  }
  }
  @media (max-width:500px){
    .skill_box:nth-child(odd) .skill_icon{
      width: 70%;
  }
  .skill_box:nth-child(odd) .skill_icon img{
    width: 60%;
  }
}
</style>






