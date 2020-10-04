<template>
<section id="portfolio" class="flex-centered-column">
  <div class="title-container">
    <div id="portfolio-title-decoration" class="titles-decoration subtitles-decoration"></div>
    <h2 class="t-header">Portfolio<span>.</span></h2>
  </div>
  <p class="t-body-primary">I love learning by doing, and these projects have fueled my motivation to discover new tecnologies and become a better developer.</p>
</section>
</template>

<script>
export default {

}
</script>

<style lang="scss">

#portfolio h2{
  position: relative;
  span{
    color: $primary-light;
  }
}

#portfolio p{
  margin: 0 $margin-regular;
}

#portfolio-title-decoration{
  width: 170px;
  background-color: $secondary-light;
  transform: skew(-50deg);

  @media (min-width: $breakpoint){
    width: 275px;
  }
}
</style>