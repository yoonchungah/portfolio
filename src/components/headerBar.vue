<template>
  <nav>
    <ul>
      <li v-on:click="gosection" data-target="Intro" class="gotosce">INTRO</li>
      <li v-on:click="gosection" data-target="About" class="gotosce">ABOUT ME</li>
      <li v-on:click="gosection" data-target="Skills" class="gotosce">SKILLS</li>
      <li v-on:click="gosection" data-target="Project" class="gotosce">PROJECT</li>
      <li v-on:click="gosection" data-target="Javascript" class="gotosce">JAVASCRIPT</li>
      <li v-on:click="gosection" data-target="Contact" class="gotosce">CONTACT</li>
    </ul>
  </nav>
</template>
<style scoped>
  nav{
    position: sticky;
    bottom:0; left: 0;
    cursor: pointer;
  }
  nav>ul{
    display: flex;
    justify-content: center;
    align-items: center;
    max-width: 1440px;
    margin: 0 auto;
    background-color: #0a0a0a;
    height: 100px;
  }
  nav>ul>li{
    font-size: 22px;
    font-weight: bold;
    color: #F3F3F3;
    margin-right: 5%;
  }
  nav>ul>li:last-child{
    margin-right: 0;
  }
</style>
<script>
  export default{
    methods : {
      gosection(e){
        //class="gotosce"가 타겟에 없으면 아무것도 하지말고 그냥 리턴 시켜라
        //다른곳에서 또 gosection를 쓸까봐 그것을 방지하고자 만든 것
        if(!e.target.matches(".gotosce")) return;
        e.preventDefault();

        const sec = document.getElementById(e.target.dataset.target);
        if(sec){
          sec.scrollIntoView({behavior : "smooth"});
        }
      },
    },
  };
</script>