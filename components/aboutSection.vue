<template>
  <section id="about">
  <h2 class="t-header">About Me.</h2>
  <p class="t-body-primary">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Consequatur reiciendis aspernatur porro amet voluptate rem nisi sapiente placeat mollitia quo quas quam ullam quisquam, ex accusamus aut, optio ipsum corporis.</p>
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

#about h2{
  margin: 100px 0px; //TODO replace with responsive units
}

#about p{
  width: 50%; //TODO finetune value
}
</style>