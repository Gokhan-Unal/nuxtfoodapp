<template>
  <main class="container">
    <app-header />
    <app-restaurant-info :datasource="fooddata" />
  </main>
</template>

<script>
import AppHeader from "../components/AppHeader.vue";
import AppRestaurantInfo from "../components/AppRestaurantInfo.vue";
import { mapState } from "vuex";

export default {
  components: { AppHeader, AppRestaurantInfo },
  name: "IndexPage",
  computed: {
    ...mapState(["fooddata"]),
  },
};
</script>
