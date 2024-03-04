<template>
  <div>
    <div class="shoppingcardlist">
      <h2>{{ card.name }}</h2>
      <h3>{{ card.cost }}</h3>
      <button v-on:click="$emit('remove')">Remove Item</button>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  card: Object,
});
</script>

<style lang="scss" scoped></style>
