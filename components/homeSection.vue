<template>
<section id="home" class="flex-centered-column">
  <div id="title-container">
    <div id="title-decoration" class="titles-decoration"></div>
    <h1 class="t-header-main">Joan Carazo - developer<span>.</span></h1>
  </div>
  <p class="t-body-bigger">I build user interfaces using Vue.js, Sass, Js and UE4/C++.<br>I love Agile development, Lean principles and component-driven design</p>
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
  width: 100%;
}

#home h1{
  position: relative;

  span{
    color: $secondary-dark;
  }
}

#home p{
  width: 70%; //TODO finetune value
}

#title-container{
  position: relative;
  margin: 100px 30px; //TODO replace with responsive units
}

#title-decoration{
  background-color: $secondary-dark;
  width: 250px;
  top: 30px;
  left: -5px;

  @media(min-width: $breakpoint){
    width: 445px;
    top: 53px;
  }
}
</style>