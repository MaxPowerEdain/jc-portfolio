<template>
  <div>
    <homeSection/>
    <aboutSection/>
    <portfolioSection/>
    <div id="projectCardContainer">
      <projectCard v-for="project in projects" 
        :key="project.id" 
        :id="project.id" 
        :projectName="project.name"
        :projectDescription="project.description"
      />
    </div>
    <contactSection/>
  </div>
</template>

<script>
import projectsJSON from '../static/projects.json';
import projectCard from '../components/projectCard';
import homeSection from '../components/homeSection';
import aboutSection from '../components/aboutSection';
import portfolioSection from '../components/portfolioSection';
import contactSection from '../components/contactSection';

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
      title: 'JC-Portfolio',
      link: [
          {
            rel: 'stylesheet',
            href: 'https://fonts.googleapis.com/css2?family=Nunito&family=Space+Mono&display=swap'
          }
        ]
    }
  }
}
</script>

<style lang="scss">
#projectCardContainer{
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
}
</style>
