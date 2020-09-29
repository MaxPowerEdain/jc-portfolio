<template>
  <main class="flex-centered-column">
    <homeSection/>
    <aboutSection/>
    <portfolioSection/>
    <div id="project-card-container" class="flex-centered-column side-margin-big">
      <projectCard v-for="(project, index) in projects"
        :key="project.id" 
        :id="project.id" 
        :projectName="project.name"
        :projectIntro="project.intro"
        :projectImage="project.image"
        :indexBasedStyle="projectColorStyles[index % 3]"
        :isEven="index % 2 === 0"
        :projectUrl="project.url"
        :projectGitHub="project.github"
        :projectAdditional="project.additional"
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
        main: colorStyles.primaryLight,
        secondary: colorStyles.primaryDark
      },
      {
        main: colorStyles.accentBright,
        secondary: colorStyles.accentColor
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

#project-card-container{
  margin-bottom: 100px;
}

</style>