<template>
  <div>
    <label :for="select">Which {{ select }} do you want?</label>

    <select :id="select" name="thing">
      <option value>-- Please select a {{ select }}</option>
      <option v-for="option in selectOptions" :key="option" value=""></option>
    </select>
  </div>
</template>

<script>
export default {
  props: {
    select: {
      type: String,
      default: "cuisine",
    },
    selectOptions: {
      type: Array,
      default: () => ["tacos", "pizza", "dim sum"],
    },
  },
};
</script>

<style lang="sass" scoped>
</style>