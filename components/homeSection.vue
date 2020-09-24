<template>
<section id="home">
  <div id="titleContainer">
    <div id="titleDecoration"></div>
    <h1 class="t-header">Joan Carazo - developer<span>.</span></h1>
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
  display: flex;
  flex-direction: column;
  align-items: center;
}

#home h1{
  position: relative;
  margin: 100px 30px; //TODO replace with responsive units
  font-size: 36px; //TODO probably move to text-global.scss
  @media (min-width: $breakpoint) {
    font-size: 64px
  }
  span{
    color: $secondary-dark;
  }
  
}

#home p{
  width: 70%; //TODO finetune value
}

#titleContainer{
  position: relative;
}

#titleDecoration{
  width: 250px;
  margin: 0 30px;
  height: 10px;
  background-color: $secondary-dark;
  transform: skew(-50deg);
  position: absolute;
  top: 130px;
  left: -5px;

  @media(min-width: $breakpoint){
    width: 445px;
    height: 18px;
    top: 153px;
  }
}
</style>