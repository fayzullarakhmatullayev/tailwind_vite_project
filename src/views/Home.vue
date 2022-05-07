<template>
  <header>
    <h2 class="text-gray-700 text-6xl font-semibold mb-4">Recipes</h2>
    <h3 class="text-2xl font-semibold">For Ninjas</h3>
  </header>

  <div>
    <h4 class="font-bold mt-12 pb-2 border-b border-gray-200">
      Latest Recipes
    </h4>
    <div
      class="mt-8 grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 xl:gap-10 lg:gap-6 gap-4"
    >
      <!-- card go here -->
      <the-card v-for="dish in menuDishes" :key="dish.id" :dish="dish" />
    </div>

    <h4 class="font-bold mt-12 pb-2 border-b border-gray-200">Most Popular</h4>
    <div class="mt-8">
      <!-- card go here -->
    </div>
    <div class="flex justify-center">
      <div
        class="btn bg-secondary-100 text-secondary-200 hover:shadow-inner transition ease-out duration-300 transform hover:scale-125 hover:opacity-50"
      >
        Load more
      </div>
    </div>
  </div>
</template>

<script setup>
import TheCard from "../components/TheCard.vue";
const menuDishes = [
  {
    id: 0,
    name: "5 Bean Chilli Stew",
    recipe_by: "Recipe by Mario",
    duration: 25,
    img: "src/assets/img/stew.jpg",
  },
  {
    id: 1,
    name: "Veg Noodles",
    recipe_by: "Recipe by Mario",
    duration: 25,
    img: "src/assets/img/noodles.jpg",
  },
  {
    id: 2,
    name: "Tofu Curry",
    recipe_by: "Recipe by Mario",
    duration: 25,
    img: "src/assets/img/curry.jpg",
  },
];
</script>
