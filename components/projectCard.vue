<template>
<nuxt-link :to="'/' + id">
  <div class="projectCard">
    <p>{{ projectName }}</p>
    <p>{{ projectDescription }}</p>
  </div>
</nuxt-link>
</template>

<script>
export default {
  name: 'projectCard',
  props: ['name', 'id', 'projectName', 'projectDescription']
}
</script>

<style>

</style>