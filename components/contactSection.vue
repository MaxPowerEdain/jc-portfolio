<template>
<section id="contact">
  <h2 class="t-header">Contact.</h2>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Et corrupti voluptates odio incidunt deserunt earum a, neque nemo sunt? Nam quam magni debitis voluptatibus possimus corrupti assumenda sint praesentium! Excepturi?</p>
</section>
</template>

<script>
export default {

}
</script>

<style lang="scss">
#contact{
  background: $primary-gradient;
  color: white;
  display: flex;
  flex-direction: column;
  align-items: center;
}

#contact h2{
  margin: 100px 0px; //TODO replace with responsive units
  font-size: 36px; //TODO probably move to text-global.scss
  @media (min-width: $breakpoint) {
    font-size: 64px
  }
}

#contact p{
  width: 50%; //TODO finetune value
}
</style>