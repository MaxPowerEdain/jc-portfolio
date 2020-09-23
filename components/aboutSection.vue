<template>
  <section id="about">
  <div id="aboutTitleContainer">
    <div id="aboutTitleDecoration"></div>
    <h2 class="t-header">About Me<span>.</span></h2>
  </div>
  <div id="aboutContainer">
    <p class="t-body-primary"><span class="t-header-small">Past</span><br>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Consequatur reiciendis aspernatur porro amet voluptate rem nisi sapiente placeat mollitia quo quas quam ullam quisquam, ex accusamus aut, optio ipsum corporis.</p>
    <p class="t-body-primary"><span class="t-header-small">Present</span><br>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Consequatur reiciendis aspernatur porro amet voluptate rem nisi sapiente placeat mollitia quo quas quam ullam quisquam, ex accusamus aut, optio ipsum corporis.</p>
    <p class="t-body-primary"><span class="t-header-small">Future</span><br>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Consequatur reiciendis aspernatur porro amet voluptate rem nisi sapiente placeat mollitia quo quas quam ullam quisquam, ex accusamus aut, optio ipsum corporis.</p>
  </div>
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss">
#about{
  height: 91vh;
  display: flex;
  flex-direction: column;
  align-items: center;
}

#aboutContainer{
  padding: 0 50px;
  display: flex;
  flex-direction: column;
  align-items: center;
  @media (min-width: $breakpoint) {
    display: grid;
    grid-template-columns: 33% 33% 33%;
    justify-items: center;
  }
}

#about h2{
  margin: 100px 0px; //TODO replace with responsive units
  position: relative;
  span{
    color: $secondary-light;
  }
}

#aboutTitleContainer{
  position: relative;
}

#aboutTitleDecoration{
  width: 248px;
  height: 18px;
  background-color: $accent-bright;
  transform: skew(-50deg);
  position: absolute;
  top: 140px;
  left: -13px;
}

#about p{
  span{
    display: block;
  }
  width: 70%; //TODO finetune value
}
</style>