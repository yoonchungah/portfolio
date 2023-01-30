<template>
 <section id="Javascript">
   <article class="script_wrap w1440">
    <h2>javascript</h2>
    <nav class="jscript_box mt100">
      <ul class="jscript mt40">
        <li><a href="#">숫자맞추기</a></li>
        <li><a href="#">todolist</a></li>
        <li><a href="#">뉴스타임즈</a></li>
      </ul>
    </nav>
   </article>
 </section>
</template>
<style scoped>
 #Javascript{
   width: 100%;
   height: 80vh;
   margin-top: 100px;
 }
  /* title */
  .script_wrap>h2{
    font-size: 40px;
    text-transform: uppercase;
    font-weight: bold;
    padding-top: 100px;
  }
  /* 리스트 */
  .jscript{
    display: flex;
    justify-content: space-between;
  }
  .jscript>li{
    width: 30%;
    height: 350px;
    border-radius: 8px;
    background-color: #1D1D1D;
  }
 @media (max-width:1280px) {
  #Javascript{
   height: 100%;
   padding-bottom: 13%;
 }
  #Javascript{
   margin-top: 0;
 }
  .script_wrap>h2{
    font-size: 1.925rem;
  }
  .jscript>li{
    height: 280px;
  }
}
@media (max-width:1000px) {
  .jscript>li{
    height: 220px;
  }
}
@media (max-width:800px) {
  .script_wrap>h2{
    font-size: 5.5vw;
  }
  .jscript{
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .jscript>li{
    width: 100%;
    height: 30vh;
    margin-bottom: 6%;
  }
  .jscript>li:last-child{
    margin-bottom: 0;
  }
}
</style>