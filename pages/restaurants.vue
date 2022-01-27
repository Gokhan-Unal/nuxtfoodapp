<template>
  <main class="container restaurant">
    <div class="restaurantheading">
      <h1>Restaurant</h1>
    </div>
    <app-restaurant-info />
  </main>
</template>

<script>
import AppRestaurantInfo from "../components/AppRestaurantInfo.vue";
export default {
  components: { AppRestaurantInfo },
};
</script>

<style lang="scss" scoped>
</style>