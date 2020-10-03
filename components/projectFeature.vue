<template>
  <div class="project-feature">
    <p class="t-header-small">{{ name }}</p>
    <img :data-src="require('~/assets/images/' + image)" :data-srcset="require('~/assets/images/' + image).srcSet" :alt="name + ' image'" class="project-feature-image lazyload">
    <p class="t-body-primary">{{ text }}</p>
  </div>
</template>

<script>
export default {
  name: 'projectFeature',
  props: ['name', 'text', 'image'],
}
</script>

<style lang="scss">

.project-feature{
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 50px 0;

  @media (min-width: $breakpoint){
    display: grid;
  grid-template-columns: auto auto;
  grid-template-rows: 30% 70%;
  width: 70%;
  }

  .project-feature-image{
    grid-column: 1 / 2;
    grid-row: 1 / 3;
    background-color: grey;
    height: 140px;
    width: 250px;
    margin: 20px;
    outline: 1px solid grey;
    transition: .2s;

    @media (min-width: $breakpoint) {
      height: 239px;
      width: 425px;
    }
  }
  
  .project-feature-image:hover{
    transform: scale(1.3);
  }
}

</style>