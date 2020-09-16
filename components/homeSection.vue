<template>
<section id="home">
  <h1 class="t-header">Joan Carazo - developer</h1>
  <p class="t-body-primary">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Placeat eveniet asperiores dignissimos, illum quae dolores sit delectus! Aliquam vel possimus non ex dolore, enim quisquam, beatae sunt odio iste voluptatem.</p>
</section>
</template>

<script>
export default {

}
</script>

<style lang="scss">
#home{
  background: $primary-gradient;
  color: white;
  height: 91vh;
  display: flex;
  flex-direction: column;
  align-items: center;
}

#home h1{
  margin: 100px 0px; //TODO replace with responsive units
  font-size: 36px; //TODO probably move to text-global.scss
  @media (min-width: $breakpoint) {
    font-size: 64px
  }
}

#home p{
  width: 50%; //TODO finetune value
}
</style>