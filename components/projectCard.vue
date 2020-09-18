<template>
<nuxt-link :to="'/' + id">
  <article class="projectCard">
    <p class="t-header-small projectName">{{ projectName }}</p>
    <p class="t-body-primary projectDescription">{{ projectDescription }}</p>
    <div class="projectCardImage"></div>
  </article>
</nuxt-link>
</template>

<script>
import style from '../assets/scss/variables.scss';

export default {
  name: 'projectCard',
  props: ['name', 'id', 'projectName', 'projectDescription'],
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
  }
}
</script>

<style lang="scss">
.projectCard{
  display: grid;
  grid-template-columns: 30% 70%;
  grid-template-rows: 30% 70%;
  grid-template-areas: 
    "projectCardImage projectName"
    "projectCardImage projectDescription";
  width: 100%;
  height: auto;
  padding: 30px 30px;
  color: white;
  text-decoration: none;
  .projectCardImage{
    width: 100px;
    height: 75px;
    background-color: grey;
    grid-area: projectCardImage;
    justify-self: center;
    align-self: center;
    @media (min-width: $breakpoint) {
      width: 200px;
      height: 150px;
    }
  }
  .projectName{ 
    grid-area: projectName;
  }
  .projectDescription{
    grid-area: projectDescription;
  }
}
a{
  text-decoration: none!important; //override Nuxt link underline on :hover
  width: 100%;
  //max-width: 90%;

  :hover{
    width: 100%!important;
  }
}
</style>