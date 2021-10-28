<template>
   <nav class='nav'>
      <p class='nav_element' @click="scroll('home')">home</p>
      <p class='nav_element' @click="scroll('about')">about</p>
      <p class='nav_element' @click="scroll('projects')">projects</p>
      <p class='nav_element' @click="scroll('contact')">contact</p>
    </nav>
     <Home id='home'/>
     <About id='about'/>
     <Projects id='projects'/>
     <Contact id='contact'/>
</template>

<script>
import Home from '@/components/Home.vue'
import About from '@/components/About.vue'
import Projects from '@/components/Projects.vue'
import Contact from '@/components/Contact.vue'

export default {
  name: 'App',
  components: {
    Home,
    About,
    Projects,
    Contact
  },
  methods:{
   scroll(id){
     document.getElementById(id).scrollIntoView({
       behavior: 'smooth'
     })
   }
  }
}
</script>

<style lang="scss">
.nav {
    position: fixed;
    display:flex;
    width: 100vw;
    z-index: 6;
    font-size: 0.7rem;
    background-color: white;

    

    &_element{
    text-transform: uppercase;
    width: 25%;
    text-align: center;
    padding: 1vh;
    color:black;
    transition: 0.2s ease-in;
    }
     &_element:hover{
    cursor: pointer;
    background-color: rgb(51, 153, 255);
    color:white;
  }
}

@media (min-width: 768px) {
  .nav{
    font-size: 0.8rem;
  }
}
@media (min-width: 1024px) {
  .nav{
    font-size: 0.85rem;
  }
}
@media (min-width: 1280px) {
  .nav{
    font-size: 0.9rem;
  }
}
@media (min-width: 1440px) {
  .nav{
    font-size: 1rem;
  }
}
</style>
