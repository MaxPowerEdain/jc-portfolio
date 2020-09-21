<template>
  <main>
    <homeSection/>
    <aboutSection/>
    <portfolioSection/>
    <div id="projectCardContainer">
      <projectCard v-for="(project, index) in projects"
        :key="project.id" 
        :id="project.id" 
        :projectName="project.name"
        :projectDescription="project.description"
        :indexBasedStyle="projectColorStyles[index % 3]"
        :isEven="index % 2 === 0"
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
import colorStyles from '../assets/scss/variables.scss';

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
      projects: [],
      projectColorStyles: [
      {
        main: colorStyles.accentBright,
        secondary: colorStyles.accentColor
      },
      {
        main: colorStyles.primaryLight,
        secondary: colorStyles.primaryDark
      },
      {
        main: colorStyles.secondaryLight,
        secondary: colorStyles.secondaryDark
      }]
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