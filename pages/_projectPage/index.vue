<template>
  <div>
    <h1>{{ project.name }}</h1>
    <p>{{ project.description }}</p>
    <p>{{ project.learning }}</p>
    <p>{{ project.problems }}</p>
  </div>
</template>

<script>
import projectsJSON from '../../static/projects.json';

export default {
  head(){
    return {
      title: 'JC-Portfolio'
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