<template>
  <div class="flex w-full min-h-screen font-sans bg-gray-800">
    <Sidebar />
    <main class="flex flex-col flex-1 gap-6 p-4">
      <header>
        <h1 class="text-3xl font-semibold leading-loose text-white">Dashboard</h1>
        <div class="text-gray-200">Tuesday 2 Feb, 2021</div>
      </header>
      <hr class="border-gray-700" />
      <StatsCard />
      <OrderReport />
    </main>
    <aside class="flex flex-col gap-y-6 pt-6 pr-6 w-96">
      <MostOrdered />
      <MostTypeOfOrder />
    </aside>
  </div>
</template>

<script setup>
import Sidebar from "./components/Sidebar.vue";
import StatsCard from "./components/StatsCard.vue";
import OrderReport from "./components/OrderReport.vue";
import MostOrdered from "./components/MostOrdered.vue";
import MostTypeOfOrder from "./components/MostTypeOfOrder.vue";
</script>
