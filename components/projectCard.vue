<template>
<nuxt-link :to="'/' + id">
  <div class="projectCard">
    <p class="t-header-small">{{ projectName }}</p>
    <p class="t-body-primary">{{ projectDescription }}</p>
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