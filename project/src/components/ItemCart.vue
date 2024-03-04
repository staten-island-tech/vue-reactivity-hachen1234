<template>
  <div>
    <div class="shoppingcardlist">
      <button class="delete" @click="remove(card)">
        Remove Item from Cart
      </button>
      <h2>{{ card.name }}</h2>
      <h3>{{ card.cost }}</h3>
    </div>
  </div>
</template>

<script setup>
import cards from "@/views/HomeView.vue";
const props = defineProps({
  card: Object,
});
function remove() {
  cards.name = "";
  cards.cost = "";
}
</script>

<style lang="scss" scoped></style>
