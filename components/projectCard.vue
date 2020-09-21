<template>
<div>
  <hr 
    :style="cardMainColor" 
    :class="isEven ? 'barEven' : 'barOdd'">
  <article class="projectCard">
    <section class="projectCardDetails">
      <p class="t-header-small projectName">{{ projectName }}</p>
      <p class="t-body-primary projectDescription">{{ projectDescription }}</p>
      <section class="projectLinks">
        <nuxt-link :to="'/' + id" class="t-button" :style="linkMainColor">Details</nuxt-link>
        <nuxt-link :to="'/' + id" class="t-button" :style="linkSecondaryColor">Visit</nuxt-link>
      </section>
    </section>
    <div class="projectCardImage"></div>
  </article>
</div>
</template>

<script>
export default {
  name: 'projectCard',
  props: ['name', 'id', 'projectName', 'projectDescription', 'indexBasedStyle', 'isEven'],
  computed: {
    cardMainColor(){
      return {
        border: `1px solid ${this.indexBasedStyle.main}`
      }
    },
    cardSecondaryColor(){
      return {
        border: `1px solid ${this.indexBasedStyle.secondary}`
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
    }

  }
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

.barEven{
  width: 50%;
  text-align: left;
  margin-left: 10%;
}

.barOdd{
  width: 50%;
  text-align: right;
  margin-right: 10%;
}

.barOdd, .barEven {
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