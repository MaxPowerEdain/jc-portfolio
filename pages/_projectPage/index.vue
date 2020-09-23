<template>
  <div>
    <h1 class="t-header">{{ project.name }}</h1>
    <p class="t-body-primary">{{ project.description }}</p>
    <p class="t-body-primary">{{ project.learning }}</p>
    <p class="t-body-primary">{{ project.problems }}</p>
  </div>
</template>

<script>
import projectsJSON from '../../static/projects.json';

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

<style>

</style>