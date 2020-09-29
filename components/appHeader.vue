<template>
<div id="nav-bar-wrapper">
  <b-navbar toggleable="lg" type="dark" variant="info" class="bg-transparent">
    <b-navbar-toggle target="nav-collapse" class="ml-auto" id="navBar-hamburger"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav class="ml-auto t-nav text-right">
        <b-nav-item to="/#home">Home</b-nav-item>
        <b-nav-item to="/#about">About Me</b-nav-item>
        <b-nav-item to="/#portfolio">Portfolio</b-nav-item>
        <b-nav-item to="/#contact">Contact</b-nav-item>
      </b-navbar-nav>

    </b-collapse>
  </b-navbar>
</div>
</template>

<script>
export default {
  name: 'appHeader',
  mounted() {
    const navBar = document.querySelector('#nav-bar-wrapper');
    const startColor = [18, 52, 141];
    const endColor = [4, 15, 87]; //todo pick from scss or background gradient
    let incrementArray = [];

    //calculates the increment/decrement between the two colors
    for(let i = 0; i < endColor.length; i++){
      incrementArray.push(endColor[i] - startColor[i]);
    }

    window.addEventListener('scroll', () =>{
      let navBarHeight = navBar.clientHeight;
      let windowHeight = window.innerHeight;
      let windowScrolled = window.scrollY;

    //calculates how much screen we scrolled (between 0 and 1)
      let scrollRatio = (windowHeight - windowScrolled)/windowHeight;
      let scrollRatioNav = (windowHeight - windowScrolled - navBarHeight * (1 - scrollRatio))/windowHeight;
      let newColor = [];
      for(let i = 0; i < incrementArray.length; i++){
        newColor.push((1 - scrollRatioNav) * incrementArray[i] + startColor[i]);
      }
      let [r, g, b] = newColor;
      r = Math.max(endColor[0], Math.min(r, startColor[0]));
      g = Math.max(endColor[1], Math.min(g, startColor[1]));
      b = Math.max(endColor[2], Math.min(b, startColor[2]));
      navBar.style.backgroundColor = `rgb(${r}, ${g}, ${b})`;
    });
  }
}
</script>

<style lang="scss">
#nav-bar-wrapper{
  position: sticky;
  z-index: 500;
  top: 0;
  background-color: $primary-light;
  color: white;
}

.nav-item.nav-item.nav-item a {
  color:white;
  :hover{
    color: white;
  }
  margin: 0 10px;
}

</style>