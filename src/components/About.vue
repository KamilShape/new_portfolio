<template>
  <section class='aboutSection'>
    <h1 class='aboutSection_header'>ABOUT</h1>
    <div class='aboutSection_photo'></div>
    <p class='aboutSection_description'>
     <strong>Hi, I'm Kamil Linstedt.</strong><br>
        I'm beginner junior front-end developer. I graduated from Civil Engineering at
        Gdansk University of technology.I've been learning programming since over a year. 
        My main goal is to get a job as junior front-end developer and developing necessary
        skills and technologies in order to be a better programmer.
    </p>
    <section class='aboutSection_logos'>
      <div class='aboutSection_logo'><i class="fab fa-js aboutSection_logo--picture"></i> <p class='aboutSection_logo--name'>JavaScript</p></div>
      <div class='aboutSection_logo'><i class="fab fa-css3-alt aboutSection_logo--picture"></i> <p class='aboutSection_logo--name'>CSS 3</p></div>
      <div class='aboutSection_logo'><i class="fab fa-html5 aboutSection_logo--picture"></i> <p class='aboutSection_logo--name'>HTML 5</p></div>
      <div class='aboutSection_logo'><i class="fab fa-vuejs aboutSection_logo--picture"></i> <p class='aboutSection_logo--name'>Vue</p></div>
      <div class='aboutSection_logo'><i class="fab fa-bootstrap aboutSection_logo--picture"></i><p class='aboutSection_logo--name'>Bootstrap 3</p></div>
      <div class='aboutSection_logo'><i class="fab fa-git-square aboutSection_logo--picture"></i><p class='aboutSection_logo--name'>Git</p></div>
    </section>
  </section>
</template>

<script>

export default {
  name: 'About',
}

</script>

<style lang='scss'>
.aboutSection {
  position: relative;
  width: 100%;
  margin: 0 auto;
  min-height: 1000px;
  height: 100vh;
  z-index: 5;
  background-color: white;
  

  &_header {
    position: relative;
    top: 30px;
    // z-index: 3;
    font-size: 1.4rem;
    padding: 10px;
    text-align: center;
  }

  &_photo {
    position: relative;
    top: 50px;
    height: 250px;
    width: 250px;
    background-image: url(../assets/zdjecie.png);
    background-position: center top;
    background-size: cover ;
    margin: 10px auto;
    border-radius: 125px;
  }

  &_description {
    position: relative;
    top: 70px;
    width: 80%;
    font-size: 0.7rem;
    padding: 15px;
    margin: 10px auto;
    text-align: center;
  }

  &_logos{
    position: relative;
    top: 90px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }

  &_logo{
    width: 50%;
  }

  &_logo--picture{
    font-size: 2rem;
    text-align: center;
    width: 100%;
  } 

  &_logo--name{
    font-size: 0.7rem;
    text-align: center;
    padding: 15px;
  }
}
@media (min-width: 414px) {
   .aboutSection {
      &_header {
      font-size: 1.5rem;
      }

      &_description {
        font-size: 0.9rem;
        top: 80px;
      }
      &_logos{
        top: 110px;
      }
      &_logo--picture{
        font-size: 3.5rem;
      } 
      &_logo--name{
        font-size: 0.9rem;
      }
  }
}

@media (min-width: 768px) {
   .aboutSection {
      &_header {
      font-size: 1.7rem;
      }

      &_description {
        font-size: 1.0rem;
      }
      &_photo {
        height: 300px;
        width: 300px;
        border-radius: 150px;
      }
      &_logo--name{
        font-size: 1.0rem;
      }
  }
}

@media (min-width: 1024px) {
    .aboutSection {
      &_header {
      font-size: 1.9rem;
      }

      &_description {
        font-size: 1.2rem;
      }
      &_photo {
        height: 350px;
        width: 350px;
        border-radius:175px;
      }
      &_logo{
        width: 16%;
      }
      &_logo--picture{
        font-size: 4.5rem;
      }
      &_logo--name{
        font-size: 1.2rem;
      }
  }
}

@media (min-width: 1280px) {
  .aboutSection {
      &_header {
      font-size: 2.1rem;
      }
      &_description {
        font-size: 1.3rem;
      }
      &_photo {
        height: 400px;
        width: 400px;
        border-radius: 200px;
      }
      &_logo--picture{
        font-size: 5rem;
      }
      &_logo--name{
        font-size: 1.3rem;
      }
  }
}

@media (min-width: 1440px) {
  .aboutSection {
    width: 70%;
     &_header {
      font-size: 2.3rem;
      }
      &_description {
        font-size: 1.4rem;
      }
       &_logo--picture{
        font-size: 5.5rem;
      }
       &_logo--name{
        font-size: 1.4rem;
      }
  }
}

</style>
