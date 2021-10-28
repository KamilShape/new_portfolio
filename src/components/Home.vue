<template>
  <section class='homeSection'>
      <div class='homeSection_circle--top homeSection_circle--first'></div>
      <div class='homeSection_circle--top homeSection_circle--second'></div>
      <div class='homeSection_circle--top homeSection_circle--third'></div>
      <div class='homeSection_circle--top homeSection_circle--fourth'></div>
      <div class='homeSection_circle--bottom homeSection_circle--first'></div>
      <div class='homeSection_circle--bottom homeSection_circle--second'></div>
      <div class='homeSection_circle--bottom homeSection_circle--third'></div>
      <div class='homeSection_circle--bottom homeSection_circle--fourth'></div>
    <transition name='show'>
      <h1 class='homeSection_header'>
      Hello, I'm Kamil Linstedt. 
     <br> I'm junior front-end developer.
     <div class="homeSection_socialMedia">
        <a href='https://github.com/KamilShape' class="homeSection_icon"><i class="fab fa-github"></i></a>
        <a href='https://www.linkedin.com/in/kamil-linstedt-506737201/' class="homeSection_icon"><i class="fab fa-linkedin"></i></a>
    </div>
    </h1> 
    </transition>
   
  </section>
</template>

<script>

export default {
  name: 'Home',
}

</script>

<style lang='scss'>

.homeSection{
  shape-outside: circle(50%);
  max-width: 100vw;
  height: 100vh;
  background-color: rgb(51, 153, 255);
  color: white;
  min-height: 1000px;


  &_circle--top{
    position: absolute;
    left:0;
    top: 0;
    border-radius:  0  0 100% 0%;
    animation: animation-first 7s infinite;
  }
    &_circle--bottom{
    position: absolute;
    right:0;
    top: 0;
    border-radius:  0  0 0% 100% ;
    animation: animation-first 7s infinite;
  }
  &_circle--first{
    z-index: 4;
    opacity: 0.5;
    width: 200px;
    height: 200px;
    background-color: rgb(51, 180, 255);
  }
   &_circle--second{
    z-index: 3;
    width: 300px;
    height: 300px;
    background-color: rgb(51, 200, 255);
  }
   &_circle--third{
    z-index: 2;
    width: 400px;
    height: 400px;
    background-color: rgb(51, 220, 255);
  }
    &_circle--fourth{
    z-index: 1;
    width: 500px;
    height: 500px;
    background-color: rgb(51, 230, 255);
  }
 
  &_header{
  font-size: 1.4rem;
  z-index: 5;
  width: 80%;
  text-align: center;
  position: absolute;
  color: black;
  top: 50%;
  left:50%;
  transform: translate(-50%,-50%);  
   animation: bounce 5s ease-in-out;
  }
  &_socialMedia{
    margin: 10px;
  }
  &_icon{
    padding: 10px;
    color: black;
  }
    @keyframes animation-first {
   
    0%{
      transform: scale(1);
  }
    50%{
      transform: scale(3);
  }
    100%{
      transform: scale(1);
  }
  }
@keyframes bounce {
      0% {
            transform: translate(-50%,-50%) scale(0);     
          }
      50% {
            transform: translate(-50%,-50%) scale(1.5);
          }
      100% {
            transform: translate(-50%,-50%) scale(1);
            }
        }
}
@media (min-width: 414px) {
  .homeSection_header{
    font-size: 1.6rem;
  }
}
@media (min-width: 768px) {
  .homeSection_header{
    font-size: 1.7rem;
  }
}
@media (min-width: 1024px) {
  .homeSection_header{
    font-size: 1.9rem;
  }
}
@media (min-width: 1280px) {
  .homeSection_header{
    font-size: 2.1rem;
  }
}
@media (min-width: 1440px) {
  .homeSection_header{
    font-size: 2.3rem;
  }
}
</style>
