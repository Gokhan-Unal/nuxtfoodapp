<template>
  <section class="restaurantinfo">
    <div v-for="store in fooddata" :key="store.id">
      <h2>{{ store.name }}</h2>
      <p>Delivery Time {{ store.deliveryTime }}</p>
      <p>Rating {{ store.rating }}</p>
      <p v-if="store.freeDelivery" class="label">
        <span>Free Delivery</span>
      </p>
      <div class="row">
        <div
          v-for="menuItem in store.menu"
          :key="menuItem.id"
          class="items"
          :style="`background:url(${menuItem.img})
          no-repeat
          center
          center`"
        >
          <div class="iteminfo">
            <div>
              <h4>
                {{ menuItem.item }}
              </h4>
              <p>${{ priceFormatting(menuItem.price) }}</p>
            </div>
            <button class="ghost">View Item ></button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { mapState } from "vuex";

export default {
  computed: {
    ...mapState(["fooddata"]),
  },
  methods: {
    priceFormatting(price) {
      return price.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
    },
  },
};
</script>

<style lang="scss" scoped>
</style>