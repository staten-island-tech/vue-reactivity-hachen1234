<template>
  <div>
    <h1>{{ card.name }}</h1>
  </div>
</template>

<script>
const props = defineProps({
  card: object,
});
import { objectToString } from "@vue/shared";
import card from "../components/CardList.vue";
console.log(card);
</script>

<style scoped></style>
