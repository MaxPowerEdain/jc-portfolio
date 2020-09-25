<template>
<section id="contact" class="flex-centered-column">
  <div class="title-container">
    <div id="contact-title-decoration" class="titles-decoration subtitles-decoration"></div>
    <h2 class="t-header">Contact<span>.</span></h2>
  </div>
  <div class="contact-icons">
    <img src="~/assets/icons/email-icon.svg" alt="email">
    <img src="~/assets/icons/github-icon.png" alt="github">
    <img src="~/assets/icons/linkedin-icon.png" alt="linkedin">
  </div>
</section>
</template>

<script>
export default {

}
</script>

<style lang="scss">
#contact{
  background: $primary-gradient;
  color: white;
  width: 100%;

  .title-container{
    margin: 50px 0!important;
  }
}

#contact h2{
  position: relative;
  span{
    color: $accent-color;
  }
}

#contact p{
  width: 50%; //TODO finetune value
}

#contact-title-decoration{
  width: 106px;
  background-color: $secondary-dark;

  @media (min-width: $breakpoint) {
    width: 218px;
  }
}

.contact-icons{
  display: flex;

  img{
    margin: 0px 15px 50px;
    height: 20px;
     width: 20px;
    @media(min-width: $breakpoint){
      margin: 25px 20px 75px;
      height: 30px;
      width: 30px;
    }
  }

  img:hover{
    opacity: 70%;
  }
}
</style>