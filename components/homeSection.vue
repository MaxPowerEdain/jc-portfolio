<template>
<section id="home">
  <div id="titleContainer">
    <div id="titleDecoration"></div>
    <h1 class="t-header">Joan Carazo - developer<span>.</span></h1>
  </div>
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
  height: 95vh;
  display: flex;
  flex-direction: column;
  align-items: center;
}

#home h1{
  position: relative;
  margin: 100px 0px; //TODO replace with responsive units
  font-size: 36px; //TODO probably move to text-global.scss
  @media (min-width: $breakpoint) {
    font-size: 64px
  }
  span{
    color: $secondary-dark;
  }
  
}

#home p{
  width: 50%; //TODO finetune value
}

#titleContainer{
  position: relative;
}

#titleDecoration{
  width: 445px;
  height: 18px;
  background-color: $secondary-dark;
  transform: skew(-50deg);
  position: absolute;
  top: 153px;
  left: -5px;
}
</style>