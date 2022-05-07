<template>
  <div class="card hover:shadow-xl transition-shadow ease-out duration-500">
    <img
      class="w-full h-44 lg:h-52 object-cover"
      :src="dish.img"
      :alt="dish.name"
    />
    <div class="m-4">
      <span class="font-bold">{{ dish.name }}</span>
      <span class="block text-gray-500 text-sm">{{ dish.recipe_by }}</span>
    </div>
    <div class="badge flex items-center">
      <svg
        class="w-5 inline-block mr-1"
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        strokeWidth="2"
      >
        <path
          strokeLinecap="round"
          strokeLinejoin="round"
          d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
        />
      </svg>
      <span>{{ dish.duration }} mins</span>
    </div>
  </div>
</template>

<script setup>
defineProps({
  dish: Object,
});
</script>
