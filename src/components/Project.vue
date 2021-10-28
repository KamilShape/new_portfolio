<template>
  <section class='project' @mouseover="visible=true" @mouseleave="visible=false">
    <div class="project_image">
      <img class='project_background' :src="feedPicture"/>
      <p class="project_name">{{name}}</p>
      <div class="project_buttons">
        <a class="project_button" :href='ghlink'>GitHub</a>
        <a class="project_button" :href='link'>Live</a>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  name: 'Project',
  props:{
      name: String,
      link: String,
      ghlink: String,
      image: String
  },
  computed:{
    feedPicture(){
      return require(`../assets/${this.image}`)
    },
  }
}

</script>

<style lang='scss'>
   @keyframes showAnimation {
    0%{
      height: 0%
    }
    100%{
      height: 50%
    }
  }
  @keyframes appearAnimation {
    0%{
      opacity: 0
    }
     10%{
      opacity: 0.1
    }
     20%{
      opacity: 0.2
    }
     30%{
      opacity: 0.3
    }
     40%{
      opacity: 0.4
    }
     50%{
      opacity: 0.5
    }
     60%{
      opacity: 0.6
    }
     70%{
      opacity: 0.7
    }
    80%{
      opacity: 0.8
    }
    90%{
      opacity: 0.9
    }
    100%{
      opacity: 1;
    }
  }
  .project{
    width: 80%;
    height: 200px;
    margin: 25px; 
    position: relative;
  
  &_image{
    position: relative;
    overflow: hidden;
    width:100%;
    height: 100%;
    border-radius: 30px;
    background-color: white;
    color: white;
  }
  &_background{
    width: 100%;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
  }
  &_name{
    position: absolute;
    color: black;
    text-align: center;
    font-size: 1rem;
    top: 10%;
    left: 50%;
    transform: translateX(-50%);
    z-index:2;
    animation: appearAnimation 0.5s ease both;
  }
  &_buttons{
    position: absolute;
    top: 60%;
    left: 50%;
    transform: translateX(-50%);
    width: 70%;
    display: flex;
    justify-content: space-evenly;
    z-index: 2;
    animation: appearAnimation 0.5s ease both;
  }
  &_button{
    padding: 7px;
    border-radius: 7px 0 7px 0;
    background-color: rgb(72, 78, 78);
    border:0px;
    outline: none;
    transition: 0.5s;
    font-size: 1rem;
    text-decoration: none;
    color: white
  }
  &_button:hover{
    cursor: pointer;
    background-color: rgb(144, 188, 187);
    border-radius: 0 10px 0 10px;
  }
  }
  .project:hover{
    cursor: pointer;
  }
@media (min-width: 768px) {
  .project{
    width: 70%;
    height: 250px;
     &_button{
        padding: 8px;
        border-radius: 8px 0 8px 0;  
  }
  }
}
@media (min-width: 1024px) {
 .project{
    width: 80%;
      &_name{
        font-size: 1.1rem;
      }
      &_button{
        padding: 9px;
        border-radius: 9px 0 9px 0;
        font-size: 1.1rem;  
  }
  }
}
@media (min-width: 1280px) {
  .project{
    width: 40%;
    height: 300px;
       &_name{
        font-size: 1.15rem;
      }
      &_button{
        font-size: 1.15rem;  
  }
  }
}

</style>
