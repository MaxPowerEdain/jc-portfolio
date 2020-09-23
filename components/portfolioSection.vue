<template>
<section id="portfolio">
  <div id="portfolioTitleContainer">
    <div id="portfolioTitleDecoration"></div>
    <h2 class="t-header">Portfolio<span>.</span></h2>
  </div>
  <p class="t-body-primary">Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga tempora perspiciatis molestiae, laborum, porro maiores vero dolorum nobis rerum veniam quas voluptate! Voluptatibus laudantium reiciendis eligendi corrupti deserunt ipsum enim.</p>
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
  width: 275px;
  height: 18px;
  background-color: $secondary-light;
  transform: skew(-50deg);
  position: absolute;
  top: 140px;
  left: -13px;
}
</style>