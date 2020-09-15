<template>
<div class="wrapper">
  <b-navbar toggleable="lg" type="dark" variant="info" class="bg-transparent">
    <b-navbar-toggle target="nav-collapse" class="ml-auto"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav class="ml-auto t-nav text-right">
        <b-nav-item href="/#home">Home</b-nav-item>
        <b-nav-item href="/#about">About Me</b-nav-item>
        <b-nav-item href="/#portfolio">Portfolio</b-nav-item>
        <b-nav-item href="/#contact">Contact</b-nav-item>
      </b-navbar-nav>

    </b-collapse>
  </b-navbar>
</div>
</template>

<script>
export default {
  name: 'appHeader'
}
</script>

<style lang="scss">
.wrapper{
  position: sticky;
  top: 0;
  background-color: $primary-light;
  color: white;
}
</style>