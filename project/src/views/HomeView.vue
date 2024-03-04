<template>
  <div>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Permanent+Marker&display=swap"
      rel="stylesheet"
    />

    <h1>Pay Up</h1>
    <div class="items">
      <CardList
        class="card"
        v-for="card in cards"
        :key="cards.name"
        :card="card"
        @add="
          console.log('damn');
          {
            array = card;
            store.push(card);
          }
          console.log(store);
        "
      />
    </div>
    <div class="cartlist">
      <shoppingcardlist
        class="card"
        v-for="card in store"
        :key="card.name"
        :card="card"
        @remove="
          console.log('pushed');
          {
            array = (index, 1);
            store.splice(index, 1);
          }
          console.log(store);
        "
      />
    </div>
  </div>
</template>

<script setup>
import CardList from "@/components/CardList.vue";
import shoppingcardlist from "@/components/ItemCart.vue";
import add from "@/components/CardList.vue";
import remove from "@/components/ItemCart.vue";
import { ref } from "vue";

const cards = [
  {
    name: "Victorian Clasped Hands Seal",
    cost: "$960.00 ",
    img: "./img/img1.webp",
    used: true,
  },
  {
    name: "19th Wonderful Antique Vintage Original Bronze Hand Statue Wax Seal C.",
    cost: "$499.99 ",
    img: "./img/img2.webp",
    used: true,
  },
  {
    name: "Victorian 18ct Gold Seal with Carnelian Base",
    cost: "$600",
    img: "./img/img3.jpg",
    used: true,
  },
  {
    name: "CRASPIRE Wax Seal Stamp",
    cost: "$3.88",
    img: "./img/img4.jpg",
    used: false,
  },
  {
    name: "18th Century Noble Coat of Arms seal with original shagreen case ",
    cost: "$2,450.00",
    img: "./img/img5.avif",
    used: true,
  },
  {
    name: "Large Size-Custom Wax Seal Stamp ",
    cost: "$33.57",
    img: "./img/img6.avif",
    used: false,
  },
  {
    name: "desk stamp wax seal Staffordshire Hand Painted UK Pottery",
    cost: "$200.39",
    img: "./img/img7.webp",
    used: false,
  },
  {
    name: "Antique Victorian Wax Seal Stamp for Letter Sealing Wax with Carnelian Handle and Brass Flower Impress",
    cost: "$165.00",
    img: "./img/img8.webp",
    used: false,
  },
  {
    name: "Antique Seal, French, Napoleon III, Palais Royale MOP Hand Disc Fede",
    cost: "$855.94",
    img: "./img/img9.avif",
    used: true,
  },
  {
    name: "Silver 925 Wax Seal Stamp (15.38g.)",
    cost: "$130.00",
    img: "./img/img10.webp",
    used: true,
  },
  {
    name: "Chinese Emperor Seal",
    cost: "$79.99",
    img: "./img/img11.avif",
    used: false,
  },
  {
    name: "Ancient Antique Bronze Royal African Ruler Wax Seal Stamp ",
    cost: "$2,999.95",
    img: "./img/img12.webp",
    used: true,
  },
  {
    name: "Handy the Seal",
    cost: "$???",
    img: "./img/handy.jpg",
    used: false,
  },
];

const store = ref([]);
</script>

<style>
body * {
  box-sizing: border-box;
  font-size: 110%;
  margin: 0;
  padding: 0;
}
.permanent-marker-regular {
  font-family: "Permanent Marker", cursive;
  font-weight: 400;
  font-style: normal;
}
h1 {
  background-color: #a8dadc;
  text-align: center;
  font-size: 3rem;
}
.items {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  background-color: #fec89a;
  border: black solid;
  float: left;
  width: 75%;
}
.cartlist {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  background-color: #fec89a;
  border: black solid;
  float: right;
  width: 25%;
}
.card {
  width: 30rem;
  margin: 1rem auto;
  border-radius: 2rem;
  background-color: #ffb5a7;
  object-fit: cover;
  border-radius: 2rem;
  justify-content: space-around;
  margin-top: 6rem;
  text-align: center;
}
img {
  width: 60%;
  object-fit: cover;
  height: 20rem;
}
</style>
