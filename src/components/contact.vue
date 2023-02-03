<template>
  <section id="Contact">
    <article class="contact_wrap w1440">
      <div class="contact_title">
        <h2>contact</h2>
        <div class="call_img">
          <img src="../assets/img/call.png" alt="call">
          <span class="send_bar send_bar1"></span>
          <span class="send_bar send_bar2"></span>
          <span class="send_bar send_bar3"></span>
        </div>
      </div>
      <div class="contact_addre mt100">
        <p>Name 윤청아</p>
        <p>Phone Number 010 9176 6530</p>
        <p>Github https://github.com/yoonchungah</p>
        <p>E-mail yca3325@gmail.com</p>
      </div>
    </article>
  </section>
</template>
<style scoped>
  #Contact{
    width: 100%;
    height: 100vh;
    background-color: #0A0A0A;
    color: #f3f3f3;
  }
  .contact_wrap{
    padding-top:8%;
    padding-bottom:8%;
  }
  .contact_title{
    display: flex;
    align-items: center;
  }
  .contact_title>h2{
    font-size: 120px;
    text-transform: uppercase;
  }
  .call_img{
    width: 100px;
    height: auto;
    margin-left: 3%;
    position: relative;
  }
  .call_img img{
    width: 100%;
  }
  .send_bar{
    position: absolute;
    display: inline-block;
    width: 4px;
    background-color: #e6e6e6;
    border-radius: 3px;
  }

  .send_bar1{
    top: -23px;
    left: 49px;
    transform: rotate(10deg);
    animation-name: oneBar;
    animation-duration:2.5s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
    animation-direction: normal;
  }

  @keyframes oneBar {
  0%   {  
    height:35px;
  }
  50%{
    height: 16px;
  }
  100%  {  
    height:0px;
    
  }
}
  .send_bar2{
    top: -13px;
    left: 80px;
    transform: rotate(35deg);
    animation-name: twoBar;
    animation-duration:2.5s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
    animation-direction: normal;
  }
  @keyframes twoBar {
  0%   {  
    height:35px;
  }
  50%{
    height: 16px;
  }
  100%  {  
    height:0px;
    
  }
}
  .send_bar3{
    top: 11px;
    left: 100px;
    transform: rotate(60deg);
    animation-name: threeBar;
    animation-duration:2.5s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
    animation-direction: normal;
  }
  @keyframes threeBar {
  0%   {  
    height:35px;
  }
  50%{
    height: 16px;
  }
  100%  {  
    height:0px;
    
  }
}
  .contact_addre p:nth-child(even){
    padding-top: 20px;
    padding-bottom: 20px;
  }
  
  @media (max-width:1280px) {
  .contact_title>h2{    
      font-size: 5.2rem;
    }
  }
    @media (max-width:800px) {
  .contact_title>h2{
    font-size: 4.85rem;
    }
    .call_img{
    width: 80px;
  }
  .send_bar1{
    top: -21px;
    left: 40px;
  }
  .send_bar2{
    left: 65px;
  }
  .send_bar3{
    top: 7px;
    left: 80px;
  }
  }
  @media (max-width:560px) {
  .call_img{
    display: none;
  }
  }
  @media (max-width:400px) {
  .contact_title>h2{
    font-size: 4rem;
    }
  }
</style>