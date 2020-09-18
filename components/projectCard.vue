<template>
<nuxt-link :to="'/' + id">
  <div class="projectCard">
    <p class="t-header-small">{{ projectName }}</p>
    <p class="t-body-primary">{{ projectDescription }}</p>
    <div class="projectCardImage"></div>
  </div>
</nuxt-link>
</template>

<script>
export default {
  name: 'projectCard',
  props: ['name', 'id', 'projectName', 'projectDescription']
}
</script>

<style lang="scss">
.projectCard{
  width: 100%;
  color: white;
  text-decoration: none;
  display: grid;
  grid-template-columns: subgrid;
  grid-template-rows: subgrid;
  background-color: green;
}
nuxt-link{
  :hover{
    text-decoration: none;
    background-color: $secondary-light;
  }
}
.projectCardImage{
  background-color: grey;
  height: 150px;
  width: 250px;
  grid-area: projectCardImage;
}

p:first-child{
  grid-area: projectName;
}

p:nth-child(2){
  grid-area: projectDescription;
}
</style>