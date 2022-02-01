<template>
  <nav>
    <ul>
      <li>
        <nuxt-link exact to="/"><app-logo /></nuxt-link>
      </li>
      <li>
        <nuxt-link to="/about">About</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/restaurants">Restaurant</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/cart">Cart</nuxt-link>
      </li>
    </ul>
  </nav>
</template>

<script>
import AppLogo from "./AppLogo.vue";

export default {
  components: {
    AppLogo,
  },
};
</script>

<style lang="scss" scoped>
</style>