<template>
  <div class="flex flex-col p-6 bg-gray-900 rounded-lg gap-y-6">
    <div class="flex justify-between items-center">
      <h2 class="text-xl font-semibold leading-loose text-white">Most Ordered</h2>
      <button class="flex gap-x-2.5 py-3 px-4 rounded-lg border border-gray-700">
        <ChevronDownIcon />
        <span class="text-sm text-white">Today</span>
      </button>
    </div>
    <hr class="border-gray-700" />
    <div class="flex flex-col gap-y-4">
      <div v-for="order in mostOrdered" class="flex gap-x-4 items-center">
        <img class="w-14 h-14" :src="`/img/${order.image}`" alt="" />
        <div class="flex flex-col gap-y-0.5">
          <div class="text-sm font-medium text-white">{{ order.name }}</div>
          <div class="text-xs text-gray-500">{{ order.count }} dishes ordered</div>
        </div>
      </div>
    </div>
    <button
      class="py-3.5 rounded-lg w-full border border-primary text-primary text-sm font-semibold"
    >
      View all
    </button>
  </div>
</template>

<script setup>
import ChevronDownIcon from "../icons/chevron-down.svg";

const mostOrdered = [
  {
    name: "Spicy seasoned seafood noodles",
    image: "food-1.png",
    count: 200,
  },
  {
    name: "Salted pasta with mushroom sauce",
    image: "food-2.png",
    count: 120,
  },
  {
    name: "Beef dumpling in hot and sour soup",
    image: "food-3.png",
    count: 80,
  },
];
</script>
