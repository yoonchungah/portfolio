<template>
 <section id="Javascript">
   <article class="script_wrap w1440">
    <h2>toy project</h2>
    <nav class="jscript_box mt40">
      <ul class="jscript mt40">
        <li class="toy1"><a href="http://toys96.dothome.co.kr/toy1/index.html"></a></li>
        <li class="toy2"><a href="http://toys96.dothome.co.kr/toy2/index.html"></a></li>
        <li class="toy3"><a href="http://toys96.dothome.co.kr/toy2/index.html"></a></li>
      </ul>
    </nav>
   </article>
 </section>
</template>
<style scoped>
 #Javascript{
 width: 100%;
 height: 100%;
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
}
.jscript>li{
  width: 32%;
  height: 400px;
  border-radius: 8px;
}
.jscript>li{
  width: 32%;
  height: 400px;
  border-radius: 8px;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: top center;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;
}
.jscript>li.toy1{
  background-image: url(../assets/img/toy1.png);
}
.jscript>li.toy2{
  background-image: url(../assets/img/toy2.png);
}
.jscript>li.toy3{
  background-image: url(../assets/img/toy3.png);
}
.jscript>li>a{
  display: block;
  width: 100%;
  height: 100%;
}
@media (max-width:1280px) {
 .script_wrap>h2{
  font-size: 1.925rem;
 }
 .jscript>li{
   height: 280px;
 }
} 
@media (max-width:1000px){
  #Javascript{
    margin-top: 5%;
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
   height: 300px;
   margin-bottom: 6%;
 }
 .jscript>li:last-child{
   margin-bottom: 0;
 }
 .jscript>li{
  background-position: top center;
}
}
</style>