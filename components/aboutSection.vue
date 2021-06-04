<template>
  <section id="about" class="flex-centered-column">
    <div class="title-container">
      <div
        id="about-title-decoration"
        class="titles-decoration subtitles-decoration"
      ></div>
      <h2 class="t-header">About Me<span>.</span></h2>
    </div>
    <div id="about-container" class="flex-centered-column">
      <p class="t-body-primary">
        <span class="t-header-small">Before,</span> I studied violin for 18
        years in Valencia, Zaragoza and Vienna, following a career as teacher
        and freelance player. I developed discipline, endurance, self-learning
        skills, motivation, and improved my mindset. After deciding for a
        change, I begun my self-teaching journey as software developer, which
        was enriched by focused guidance and training in Factoria F5 Bootcamp.
      </p>
      <p class="t-body-primary">
        <span class="t-header-small">Now,</span> I work at the startup Nokues as
        a fullstack developer using Nuxt.js and Symfony. It is very motivating
        to apply tech solutions to real problems from clients and users. I also
        have fun contributing as C++ developer in BFME Reforged videogame, using
        Unreal Engine.
      </p>
      <p class="t-body-primary">
        <span class="t-header-small">Next,</span> I am deepening my knowledge of
        Software Architecture, Design Patterns and Algorithms. My goal is to
        become a versatile developer which can use different tech stacks with
        flexibility, while delivering well-crafted software and solving people's
        needs with creativity and experience.
      </p>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
#about-container {
  margin: 0 $margin-regular;

  @media (min-width: $breakpoint) {
    display: grid;
    grid-template-columns: 33% 33% 33%;
    justify-items: center;
    align-items: flex-start;
  }

  p {
    @media (min-width: $breakpoint) {
      margin: 0 $margin-regular;
    }
  }

  span {
    text-align: left;
    margin-bottom: 5px !important;
    display: block;

    @media (min-width: $breakpoint) {
      margin-bottom: 10px !important;
    }
  }
}

#about h2 {
  position: relative;
  span {
    color: $secondary-light;
  }
}

#about-title-decoration {
  width: 152px;
  background-color: $accent-bright;

  @media (min-width: $breakpoint) {
    width: 248px;
  }
}
</style>
