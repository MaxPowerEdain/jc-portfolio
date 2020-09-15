<template>
  <div>
    <homeSection/>
    <aboutSection/>
    <portfolioSection/>
    <projectCard v-for="project in projects" 
      :key="project.id" 
      :id="project.id" 
      :projectName="project.name"
      :projectDescription="project.description"
    />
    <contactSection/>
  </div>
</template>

<script>
import projectsJSON from '../static/projects.json';
import projectCard from '../components/projectCard';
import homeSection from '../components/homeSection';
import aboutSection from '../components/aboutSection';
import portfolioSection from '../components/portfolioSection';
import contactSection from '../components/contactSection'

export default {
  components: {
    projectCard,
    homeSection,
    aboutSection,
    portfolioSection,
    contactSection
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
