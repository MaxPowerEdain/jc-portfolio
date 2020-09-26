<template>
  <section id="about" class="flex-centered-column">
  <div class="title-container">
    <div id="about-title-decoration" class="titles-decoration subtitles-decoration"></div>
    <h2 class="t-header">About Me<span>.</span></h2>
  </div>
  <div id="about-container" class="flex-centered-column">
    <p class="t-body-primary"><span class="t-header-small">Before,</span>
    I studied violin for 18 years in Valencia, Zaragoza and Vienna, following a carrear as teacher, freelance orchestral player and soloist. I developed discipline, endurance, self-learning skills, motivation, and improvement mindset.</p>
    <p class="t-body-primary"><span class="t-header-small">Now,</span>
    I have finished a Frontend Bootcamp in Factoría F5, where I learned about Agile development, teamwork, and modern web-development tecnologies and tools. I continue gaining knowledge in their Fullstack Bootcamp. And I also strenghten my programming skills by coding C++ in UE4 as UI developer in the fan-project BFME Reforged.</p>
    <p class="t-body-primary"><span class="t-header-small">Next,</span>
    I am deepening my knowledge of Vue.js and backend languages and frameworks. In the future, I look forward to work with Cloud-based solutions to build the backend for flexible and scalable apps. Other areas of interest/specialization include low-level programming (C/C++) and web/cloud security management.</p>
  </div>
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss">

#about-container{
  margin: 0 $margin-regular;

  @media (min-width: $breakpoint) {
    display: grid;
    grid-template-columns: 33% 33% 33%;
    justify-items: center;
    align-items: flex-start;
  }

  p{
    @media(min-width: $breakpoint){
      margin: 0 $margin-regular;
    }
  }

  span{
    text-align: left;
    margin-bottom: 5px!important;
    display: block;

    @media(min-width: $breakpoint){
      margin-bottom: 10px!important;
    }
  }
}

#about h2{
  position: relative;
  span{
    color: $secondary-light;
  }
}

#about-title-decoration{
  width: 124px;
  background-color: $accent-bright;

  @media (min-width: $breakpoint) {
    width: 248px;
  }
}
</style>