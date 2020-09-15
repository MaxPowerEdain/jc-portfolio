<template>
  <div>
    <h1 id="home">Portfolio Home</h1>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Placeat eveniet asperiores dignissimos, illum quae dolores sit delectus! Aliquam vel possimus non ex dolore, enim quisquam, beatae sunt odio iste voluptatem.</p>
    
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Placeat eveniet asperiores dignissimos, illum quae dolores sit delectus! Aliquam vel possimus non ex dolore, enim quisquam, beatae sunt odio iste voluptatem.</p>
    
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Placeat eveniet asperiores dignissimos, illum quae dolores sit delectus! Aliquam vel possimus non ex dolore, enim quisquam, beatae sunt odio iste voluptatem.</p>
    
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Placeat eveniet asperiores dignissimos, illum quae dolores sit delectus! Aliquam vel possimus non ex dolore, enim quisquam, beatae sunt odio iste voluptatem.</p>
    <h2 id="about">About</h2>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Consequatur reiciendis aspernatur porro amet voluptate rem nisi sapiente placeat mollitia quo quas quam ullam quisquam, ex accusamus aut, optio ipsum corporis.</p>
    <h2 id="portfolio">Portfolio</h2>
    <projectCard v-for="project in projects" 
      :key="project.id" 
      :id="project.id" 
      :projectName="project.name"
      :projectDescription="project.description"
    />
    <h2 id="contact">Contact</h2>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Et corrupti voluptates odio incidunt deserunt earum a, neque nemo sunt? Nam quam magni debitis voluptatibus possimus corrupti assumenda sint praesentium! Excepturi?</p>
  </div>
</template>

<script>
import projectsJSON from '../static/projects.json';
import projectCard from '../components/projectCard';

export default {
  components: {
    projectCard
  },
  data() {
    return {
      projects: []
    }
  },
  created() {
    this.projects = projectsJSON;
  },
  head(){
    return {
      title: 'JC-Portfolio'
    }
  }
}
</script>

<style>

</style>
