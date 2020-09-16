<template>
<section id="portfolio">
  <h2 class="t-header">Portfolio</h2>
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
}

#portfolio p{
  width: 50%; //TODO finetune value, maybe move to variables if all use same width
}
</style>