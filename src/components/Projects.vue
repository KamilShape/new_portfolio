<template>
  <section class='projectsSection'>
    <h1 class='projectsSection_header'>PROJECTS</h1>
    <div class="projectsSection_projects">
      <Project
      v-for='project in projects'
      :key='project.name'
      :name='project.name'
      :link='project.link'
      :ghlink='project.ghlink'
      :image='project.image'
      />
    </div>
  </section>
</template>

<script>
import projects from '@/assets/data.js'
import Project from '@/components/Project.vue'
export default {
  data(){
    return{
      projects
    }
  },
  name: 'Projects',
  components:{
    Project
  }
}

</script>

<style lang='scss'>
.projectsSection {
  min-height: 100vh;
  background-color: rgb(187,234,255);
  padding: 10px;
  box-sizing: border-box;

  &_projects{ 
    width: 100%;
    justify-content: space-evenly;
    margin: 0 auto;
    margin-top: 50px;
    display: flex;
    flex-wrap: wrap;
  }

  &_header {
    position: relative;
    top: 30px;
    font-size: 1.4rem;
    padding: 10px;
    text-align: center;
  }
}
@media (min-width: 414px) {
  .projectsSection{
    &_projects{
      width: 70%;
    }
    &_header{
    font-size: 1.5rem;
  }
  }
}

@media (min-width: 768px) {
  .projectsSection{
    &_projects{
      width: 60%;
    }
    &_header{
    font-size: 1.7rem;
  }
  }
}
  

@media (min-width: 1024px) {
   .projectsSection{
    &_projects{
      width: 50%;
    }
    &_header{
    font-size: 1.9rem;
  }
  }
}
@media (min-width: 1280px) {
  .projectsSection{
    &_projects{
      width: 80%;
    }
    &_header{
    font-size: 2.1rem;
  }
  }
}
@media (min-width: 1440px) {
  .projectsSection{
    &_projects{
      width: 70%;
    }
    &_header{
    font-size: 2.3rem;
  }
  }
}
</style>
