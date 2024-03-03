<template>
  <div>
    <h2>{{ card.name }}</h2>
    <h3>{{ card.cost }}</h3>
  </div>
</template>

<script setup>
const props = defineProps({
  card: Object,
});
</script>

<style lang="scss" scoped></style>
