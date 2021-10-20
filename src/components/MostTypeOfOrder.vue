<template>
  <div class="flex flex-col p-6 bg-gray-900 rounded-lg gap-y-6">
    <div class="flex justify-between items-center">
      <h2 class="text-xl font-semibold leading-loose text-white">Most type of order</h2>
      <button class="flex gap-x-2.5 py-3 px-4 rounded-lg border border-gray-700">
        <ChevronDownIcon />
        <span class="text-sm text-white">Today</span>
      </button>
    </div>
    <hr class="border-gray-700" />
    <div class="flex gap-x-7">
      <img width="176" src="/img/chart.svg" alt="" />
      <div class="flex flex-col gap-y-4">
        <div class="flex gap-x-2 items-start">
          <div class="w-4 h-4 mt-0.5 rounded-full bg-accent-red" />
          <div>
            <div class="text-sm font-medium text-white">Dine in</div>
            <div class="text-xs text-gray-500">200 customers</div>
          </div>
        </div>
        <div class="flex gap-x-2 items-start">
          <div class="w-4 h-4 mt-0.5 rounded-full bg-accent-orange" />
          <div>
            <div class="text-sm font-medium text-white">To go</div>
            <div class="text-xs text-gray-500">122 customers</div>
          </div>
        </div>
        <div class="flex gap-x-2 items-start">
          <div class="w-4 h-4 mt-0.5 rounded-full bg-accent-blue" />
          <div>
            <div class="text-sm font-medium text-white">Delivery</div>
            <div class="text-xs text-gray-500">264 customers</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import ChevronDownIcon from "../icons/chevron-down.svg";
</script>
