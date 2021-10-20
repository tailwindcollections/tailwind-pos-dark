<template>
  <div class="p-6 bg-gray-900 rounded-lg">
    <div class="flex justify-between items-center pb-4">
      <h2 class="text-xl font-semibold leading-loose text-white">Order Report</h2>
      <button class="flex py-3 px-4 rounded-lg border border-gray-700 gap-x-2.5">
        <OptionsIcon />
        <span class="text-sm text-white">Filter order</span>
      </button>
    </div>
    <table class="w-full">
      <thead>
        <tr class="text-sm font-semibold text-white">
          <td class="py-4 border-b border-gray-700">Customer</td>
          <td class="py-4 border-b border-gray-700">Menu</td>
          <td class="py-4 border-b border-gray-700 text-right">Total Payment</td>
          <td class="py-4 border-b border-gray-700 text-center">Status</td>
        </tr>
      </thead>
      <tbody>
        <tr v-for="order in orders" class="text-sm text-gray-500">
          <td class="py-4">
            <div class="flex gap-4 items-center">
              <img width="32" :src="`/img/${order.avatar}`" alt="" />
              <span> {{ order.name }} </span>
            </div>
          </td>
          <td class="py-4">{{ order.menu }}</td>
          <td class="py-4 tabular-nums text-right">{{ order.total }}</td>
          <td class="py-4 flex justify-center">
            <span
              class="flex justify-center py-1 w-24 font-medium capitalize rounded-full"
              :class="{
                'bg-accent-green/20 text-accent-green': order.status === 'completed',
                'bg-accent-purple/20 text-accent-purple': order.status === 'preparing',
                'bg-accent-orange/20 text-accent-green': order.status === 'pending',
              }"
            >
              {{ order.status }}
            </span>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup>
import OptionsIcon from "../icons/options.svg";

const orders = [
  {
    avatar: "avatar-1.png",
    name: "Eren Jaegar",
    menu: "Spicy seasoned seafood noodles",
    total: "$125",
    status: "completed",
  },
  {
    avatar: "avatar-2.png",
    name: "Reiner Braunn",
    menu: "Salted Pasta with mushroom sauce",
    total: "$145",
    status: "preparing",
  },
  {
    avatar: "avatar-3.png",
    name: "Levi Ackerman",
    menu: "Beef dumpling in hot and sour soup",
    total: "$105",
    status: "pending",
  },
  {
    avatar: "avatar-4.png",
    name: "Historia Reiss",
    menu: "Hot spicy fried rice with omelet",
    total: "$45",
    status: "completed",
  },
  {
    avatar: "avatar-5.png",
    name: "Armin Arlert",
    menu: "Spicy seasoned seafood noodles",
    total: "$125",
    status: "completed",
  },
  {
    avatar: "avatar-6.png",
    name: "Hanji Zoe",
    menu: "Hot spicy fried rice with omelet",
    total: "$245",
    status: "completed",
  },
];
</script>
