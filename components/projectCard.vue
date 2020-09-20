<template>
<div>
  <svg height="2" width="700">
    <line x1="0" y1="0" x2="700" y2="0" style="stroke:rgb(255,0,0);stroke-width:3" />
  </svg>
  <article class="projectCard">
    <section class="projectCardDetails">
      <p class="t-header-small projectName">{{ projectName }}</p>
      <p class="t-body-primary projectDescription">{{ projectDescription }}</p>
      <section class="projectLinks">
        <nuxt-link :to="'/' + id" class="t-button">Details</nuxt-link>
        <nuxt-link :to="'/' + id" class="t-button">Visit</nuxt-link>
      </section>
    </section>
    <div class="projectCardImage"></div>
  </article>
</div>
</template>

<script>
export default {
  name: 'projectCard',
  props: ['name', 'id', 'projectName', 'projectDescription']
}
</script>

<style lang="scss">
.projectCard{
  display: grid;
  grid-template-columns: 50% 50%;
  grid-template-rows: 100%;
}

.projectCardImage{
  grid-column: 1 / 2;
  grid-row: 1 / 2;
  height: 150px;
  width: 250px;
  background-color: grey;
  border: 1px solid black;
  justify-self: end;
  margin: 30px;
  @media (min-width: $breakpoint) {
    height: 250px;
    width: 400px;
  }
}

.projectCardDetails{
  grid-column: 2 / 3;
  grid-row: 1 / 2;
  padding: 30px;
  max-width: 450px;
}

.projectLinks{
  display: flex;
  justify-content: flex-end;
  a{
    color: black;
    margin: 15px;
  }
}


a{
  text-decoration: none!important; //override Nuxt link underline on :hover
}
</style>