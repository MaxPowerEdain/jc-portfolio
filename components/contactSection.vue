<template>
<section id="contact">
  <div id="contactTitleContainer">
    <div id="contactTitleDecoration"></div>
    <h2 class="t-header">Contact<span>.</span></h2>
  </div>
  <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Et corrupti voluptates odio incidunt deserunt earum a, neque nemo sunt? Nam quam magni debitis voluptatibus possimus corrupti assumenda sint praesentium! Excepturi?</p>
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
  display: flex;
  flex-direction: column;
  align-items: center;
}

#contact h2{
  margin: 100px 0px; //TODO replace with responsive units
  position: relative;
  span{
    color: $accent-color;
  }
}

#contact p{
  width: 50%; //TODO finetune value
}

#contactTitleContainer{
  position: relative;
}

#contactTitleDecoration{
  width: 218px;
  height: 18px;
  background-color: $secondary-dark;
  transform: skew(-50deg);
  position: absolute;
  top: 140px;
  left: -13px;
}
</style>