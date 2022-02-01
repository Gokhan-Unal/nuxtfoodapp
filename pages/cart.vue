<template>
  <div class="container cart">
    <h2>Cart</h2>
    <section v-if="cart.length">
      <table>
        <thead>
          <tr>
            <th>Item</th>
            <th>Add Ons</th>
            <th>Amount</th>
            <th>Total Price</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in cart" :key="item.id">
            <td>
              {{ item.item }}
              <span v-if="item.options">- {{ item.options }}</span>
            </td>
            <td>
              <span v-for="addon in item.addOns" :key="addon" class="comma">{{
                addon
              }}</span>
            </td>
            <td>{{ item.count }}</td>
            <td>${{ item.combinedPrice }}</td>
          </tr>
          <tr>
            <td colspan="3"></td>
            <td class="total">${{ totalPrice.toFixed(2) }}</td>
          </tr>
        </tbody>
      </table>
    </section>
    <app-empty-cart v-else />
  </div>
</template>

<script>
import { mapState, mapGetters } from "vuex";
import AppEmptyCart from "../components/AppEmptyCart.vue";

export default {
  components: { AppEmptyCart },
  computed: {
    ...mapState(["cart"]),
    ...mapGetters(["totalPrice"]),
  },
};
</script>

<style lang="scss" scoped>
</style>