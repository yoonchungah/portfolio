<template>
  <section id="Contact">
    <article class="contact_wrap w1440">
      <h2>contact</h2>
      <div class="contact_addre mt100">
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
  .contact_wrap>h2{
    font-size: 120px;
    text-transform: uppercase;
  }
  .contact_addre p:nth-child(2){
    padding-top: 20px;
    padding-bottom: 20px;
  }

  @media (max-width:1280px) {
  .contact_wrap>h2{    
      font-size: 5.2rem;
    }
  }
    @media (max-width:800px) {
  .contact_wrap>h2{
    font-size: 4.85rem;
    }
  }
  @media (max-width:400px) {
  .contact_wrap>h2{
    font-size: 4rem;
    }
  }
</style>