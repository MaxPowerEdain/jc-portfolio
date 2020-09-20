<template>
  <main>
    <homeSection/>
    <aboutSection/>
    <portfolioSection/>
    <div id="projectCardContainer">
      <projectCard v-for="(project, index) in projects" :class="{'blue': index % 2 === 0}"
        :key="project.id" 
        :id="project.id" 
        :projectName="project.name"
        :projectDescription="project.description"
      />
    </div>
    <contactSection/>
  </main>
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
main{
  display: flex;
  flex-direction: column;
  align-items: center;
}

#projectCardContainer{
  width: 80%;
  display: flex;
  justify-self: center;
  flex-direction: column;
}
</style>