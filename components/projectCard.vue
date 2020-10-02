<template>
<div class="flex-centered-column">
  <hr 
    :style="cardMainColor" 
    :class="isEven ? 'bar-even' : 'bar-odd'">
  <article class="project-card flex-centered-column">
    <p class="t-header-small">{{ projectName }}</p>
    <img :src="require('~/assets/images/' + projectImage)" :alt="projectImage" class="project-card-image">
    <p class="t-body-primary">{{ projectIntro }}</p>
    <section class="project-links">
      <nuxt-link :to="'/' + id" class="t-button" :style="linkMainColor">Details</nuxt-link>
      <a v-if="projectUrl" :href="projectUrl" target="_blank" class="t-button" :style="linkSecondaryColor">Visit</a>
    </section>
  </article>
</div>
</template>

<script>
export default {
  name: 'projectCard',
  props: ['name', 'id', 'projectName', 'projectIntro', 'projectImage', 'indexBasedStyle', 'isEven', 'projectUrl', 'projectGitHub', 'projectAdditionals'],
  computed: {
    cardMainColor(){
      return {
        'border-top': `2px solid ${this.indexBasedStyle.main}`
      }
    },
    linkMainColor(){
      return {
        'border-bottom': `2px solid ${this.indexBasedStyle.main}`
      }
    },
    linkSecondaryColor(){
      return {
        'border-bottom': `2px solid ${this.indexBasedStyle.secondary}`
      }
    },
  }
}
</script>

<style lang="scss">
.project-card{
margin: 0 $margin-regular;

  @media (min-width: $breakpoint){
    display: grid!important;
    grid-template-columns: 50% 50%;
    grid-template-rows: 75px 1fr 75px;
  }
}

.project-card-image{
  height: 140px;
  width: 250px;
  justify-self: end;
  margin: 30px;
  
  @media (min-width: $breakpoint) {
    height: 281px;
    width: 500px;
    grid-column: 1 / 2;
    grid-row: 1 / 4;
    align-self: flex-start;
    margin: 15px 30px;
  }
}

.project-card-details{
  grid-column: 2 / 3;
  grid-row: 1 / 2;
  padding: 30px;
  max-width: 450px;
}

.project-links{
  display: flex;
  justify-content: center;

  @media (min-width: $breakpoint){
    justify-content: flex-end;
  }

  a{
    color: black;
    margin: 15px;
  }
}

.bar-even{
  text-align: left;
  margin-left: 10%;
}

.bar-odd{
  text-align: right;
  margin-right: 10%;
}

.bar-odd, .bar-even {
  width: 50%;
  margin-top: 50px;
  margin-bottom: 50px;
  @media (min-width: $breakpoint) {
    margin-top: 100px;
    margin-bottom: 100px;
  }
}

a{
  text-decoration: none!important; //override Nuxt link underline on :hover
  padding-bottom: 10px;
}
</style>