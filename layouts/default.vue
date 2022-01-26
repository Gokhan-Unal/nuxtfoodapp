<template>
  <div>
    <div class="content">
      <app-menu />
      <Nuxt />
    </div>
    <Footer />
  </div>
</template>

<script>
import AppMenu from "../components/AppMenu.vue";
import Footer from "../components/Footer.vue";
export default {
  components: { AppMenu, Footer },
};
</script>

<style lang="scss">
html {
  font-family: "Mullish", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  font-weight: 300;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: inherit;
  margin: 0;
}
h1,
h2,
h3,
h4 {
  font-family: "Poppins", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  font-weight: 600;
}
</style>