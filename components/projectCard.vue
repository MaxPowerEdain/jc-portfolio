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
  background-color: $secondary-dark;
  color: white;
  text-decoration: none;
}
nuxt-link{
  :hover{
    text-decoration: none;
    background-color: $secondary-light;
  }
}
.projectCardImage{
  background-color: white;
  height: 150px;
  width: 250px;
}
</style>