<template>
  <div class="project-feature">
    <p class="t-header-small">{{ name }}</p>
    <div class="project-feature-image">{{ image }}</div> 
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
  width: 90%;
  margin: 30px 0;

  p{
    margin-left: 20px;
  }

  @media (min-width: $breakpoint){
    display: grid;
  grid-template-columns: auto auto;
  grid-template-rows: 30% 70%;
  width: 60%;
  }

  .project-feature-image{
    grid-column: 1 / 2;
    grid-row: 1 / 3;
    background-color: grey;
    height: 130px;
    width: 130px;
    margin: 20px;

    @media (min-width: $breakpoint) {
      height: 180px;
      width: 180px;
    }
  }
}

</style>