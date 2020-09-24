<template>
  <div id="projectPage">
    <h1 class="t-header">{{ project.name }}</h1>
    <p class="t-body-primary">{{ project.description }}</p>
    <projectFeature v-for="(feature, index) in project.features"
    :key="index"
    :name = feature.name
    :text = feature.text
    :image = feature.image
    />
    <p class="t-body-primary projectLearning">{{ project.learning }}</p>
    <p class="t-body-primary projectProblems">{{ project.problems }}</p>
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

#projectPage{
  display: flex;
  flex-direction: column;
  align-items: center;

  h1{
    width: 80%;
    margin: 50px 0;
    text-align: center;
  }

  p{
    width: 80%;
  }
}

.projectLearning{
  display: flex;
  align-self: flex-end;
  background-color: $secondary-dark;
  color: white;
  width: 75%;
  justify-content: flex-start;
  text-align: left;
  padding: 20px 40px;
  margin: 0;
}

.projectProblems{
  display: flex;
  align-self: flex-start;
  background-color: $accent-color;
  color: white;
  width: 75%;
  justify-content: flex-end;
  text-align: right;
  padding: 20px 40px;
  margin: 0;
}

</style>