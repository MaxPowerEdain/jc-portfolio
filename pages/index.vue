<template>
  <div>
    <homeSection/>
    <aboutSection/>
    <portfolioSection/>
    <div id="projectCardContainer">
      <projectCard class="projectCardTemplate" v-for="project in projects" 
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
import style from '../assets/scss/variables.scss';

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
  mounted(){
    const projectCards = document.querySelectorAll(".projectCard");
    let colours = [];
    for(let color in style){
      colours.push(style[color]);
    }

    //iterates through the projectCards and assigns color from colour array
    let i = 0;
    projectCards.forEach(projectCardInstance => {
      projectCardInstance.style.backgroundColor = colours[i%colours.length];
      i++;
    });
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
.projectCardTemplate{
  display: grid;
  grid-template-rows: 30% 70%;
  height: auto;
  width: 100%;
}

.projectCardTemplate:nth-child(odd){
  grid-template-columns: 70% 250px ;
  text-align: right;
  grid-template-areas: 
    "projectName projectCardImage" 
    "projectDescription projectCardImage";
}
.projectCardTemplate:nth-child(even){
  grid-template-columns: 250px 70%;
  grid-template-areas: 
    "projectCardImage projectName" 
    "projectCardImage projectDescription";
  color: green;
  }
</style>
