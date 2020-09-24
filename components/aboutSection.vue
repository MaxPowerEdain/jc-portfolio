<template>
  <section id="about">
  <div id="aboutTitleContainer">
    <div id="aboutTitleDecoration"></div>
    <h2 class="t-header">About Me<span>.</span></h2>
  </div>
  <div id="aboutContainer">
    <p class="t-body-primary"><span class="t-header-small">Before,</span><br>I studied violin for 18 years in Valencia, Zaragoza and Vienna, following a carrear as teacher, freelance orchestral player and soloist. I developed discipline, endurance, self-learning skills, motivation, and improvement mindset.</p>
    <p class="t-body-primary"><span class="t-header-small">Now,</span><br>I have finished a Frontend Bootcamp in Factoría F5, where I learned about Agile development, teamwork, and modern web-development tecnologies and tools. I continue gaining knowledge in their Fullstack Bootcamp. And I also strenghten my programming skills by coding C++ in UE4 as UI developer in the fan-project BFME Reforged.</p>
    <p class="t-body-primary"><span class="t-header-small">Next,</span><br>I am deepening my knowledge of Vue.js and backend languages and frameworks. In the future, I look forward to work with Cloud-based solutions to build the backend for flexible and scalable apps. Other areas of interest/specialization include low-level programming (C/C++) and web/cloud security management.</p>
  </div>
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss">
#about{
  display: flex;
  flex-direction: column;
  align-items: center;
}

#aboutContainer{
  padding: 0 50px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
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
  width: 124px;
  height: 10px;
  background-color: $accent-bright;
  transform: skew(-50deg);
  position: absolute;
  top: 119px;
  left: -6px;

  @media (min-width: $breakpoint) {
    width: 248px;
    height: 18px;
    top: 140px;
    left: -13px;
  }
}

#about p{
  span{
    display: block;
    margin: 0;
  }
  width: 75%; //TODO finetune value
}
</style>