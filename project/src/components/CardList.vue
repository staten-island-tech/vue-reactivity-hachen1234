<template>
  <div>
    <div class="Cardlist">
      <h2>{{ card.name }}</h2>
      <img :src="card.img" alt="" />
      <h3>{{ card.cost }}</h3>
      <button v-on:click="$emit('add')">add to cart</button>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  card: Object,
});
</script>

<style scoped></style>
