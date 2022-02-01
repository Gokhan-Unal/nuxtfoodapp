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
    </ul>
    <div class="smallnum" v-if="cartCount > 0">{{ cartCount }}</div>
    <nuxt-link to="/cart">Cart</nuxt-link>
  </nav>
</template>

<script>
import AppLogo from "./AppLogo.vue";
import { mapGetters } from "vuex";

export default {
  computed: {
    ...mapGetters(["cartCount"]),
  },

  components: {
    AppLogo,
  },
};
</script>

<style lang="scss" scoped>
</style>