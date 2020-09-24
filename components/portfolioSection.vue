<template>
<section id="portfolio">
  <div id="portfolioTitleContainer">
    <div id="portfolioTitleDecoration"></div>
    <h2 class="t-header">Portfolio<span>.</span></h2>
  </div>
  <p class="t-body-primary">I love learning by doing, and this projects have fueled my motivation to discover new tecnologies and become a better developer.</p>
</section>
</template>

<script>
export default {

}
</script>

<style lang="scss">
#portfolio{
  display: flex;
  flex-direction: column;
  align-items: center;
}

#portfolio h2{
  margin: 100px 0px; //TODO replace with responsive units
  position: relative;
  span{
    color: $primary-light;
  }
}

#portfolio p{
  width: 50%; //TODO finetune value, maybe move to variables if all use same width
}

#portfolioTitleContainer{
  position: relative;
}

#portfolioTitleDecoration{
  width: 135px;
  height: 10px;
  background-color: $secondary-light;
  transform: skew(-50deg);
  position: absolute;
  top: 120px;
  left: -6px;

  @media (min-width: $breakpoint){
    width: 275px;
    height: 18px;
    top: 140px;
    left: -13px;
  }
}
</style>