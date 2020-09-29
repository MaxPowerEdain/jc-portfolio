<template>
  <div id="project-page" class="flex-centered-column">
    <h1 class="t-header">{{ project.name }}</h1>
    <p class="t-body-primary">{{ project.description }}</p>
    <iframe v-if="project.additional" width="560" height="315" src="https://www.youtube.com/embed/nUxWkpTr6F4?start=149" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    <section class="project-links">
      <a v-if="project.github" :href="project.github" class="t-button">Github</a>
      <a v-if="project.url" :href="project.url" class="t-button">Visit</a>
    </section>
    <projectFeature v-for="(feature, index) in project.features"
    :key="index"
    :name = feature.name
    :text = feature.text
    :image = feature.image
    />
    <p class="t-body-primary project-learning project-bottom-blocks">
      <span class="t-header-small">Learning: </span>{{ project.learning }}
    </p>
    <p class="t-body-primary project-problems project-bottom-blocks">
      <span class="t-header-small">Problems: </span>{{ project.problems }}
    </p>
  </div>
</template>

<script>
import projectsJSON from '../../static/projects.json';
import projectFeature from '../../components/projectFeature';

export default {
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
  },
  components: {
    projectFeature
  },
  data() {
    return {
      project: {}
    }
  },
  created() {
    this.project = projectsJSON.find((project)=>project.id === this.$route.params.projectPage);
  },
}

</script>

<style lang="scss">

#project-page{

  h1{
    margin: 50px 0;
    text-align: center;
  }

  p{
    margin: 0 $margin-regular;
  }
}

.project-learning{
  align-self: flex-end;
  background-color: $secondary-dark;
  justify-content: flex-start;
  text-align: left;
}

.project-problems{
  align-self: flex-start;
  background-color: $accent-color;
  justify-content: flex-end;
  text-align: right;
}

.project-bottom-blocks{
  color: white; 
  width: 100%; 
  padding: 20px 40px; 
  margin: 0!important;

  @media(min-width: $breakpoint){
    width: 75%;
  }
}

iframe{
  margin: 50px;
}

.project-links{
  margin: 50px 0;
}

.project-links a {
  color: black;
  text-decoration: none;
  padding-bottom: 10px;
  border-bottom: 2px solid $accent-bright;
  margin: 0 10px;
}

.project-links a:nth-child(2){
  border-bottom: 2px solid $secondary-dark;
}

</style>