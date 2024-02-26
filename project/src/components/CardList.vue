<template>
  <div>
    <div class="Cardlist">
      <h2>{{ card.name }}</h2>
      <img :src="card.img" alt="" />
      <h3>{{ card.price }}</h3>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  card: Object,
});
</script>

<style scoped></style>
