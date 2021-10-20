<template>
  <div class="flex flex-col gap-y-4 items-center py-8 w-24 bg-gray-900">
    <button class="p-2 bg-opacity-20 rounded-xl bg-primary">
      <StoreIcon />
    </button>
    <div class="flex flex-col gap-y-4 items-end self-end">
      <div
        v-for="menu in menus"
        :class="
          activeMenu === menu.name
            ? 'bg-gray-800 rounded-l-xl relative before:absolute before:w-4 before:h-8 before:-top-8 before:rounded-br-xl before:right-0 before:shadow-inverse-top  after:absolute after:w-4 after:h-8 after:-bottom-8 after:rounded-tr-xl after:right-0 after:shadow-inverse-bottom'
            : ''
        "
      >
        <button
          class="p-4 my-4 mr-4 ml-3 rounded-xl"
          @click="activeMenu = menu.name"
          :class="
            activeMenu === menu.name
              ? 'text-white shadow-primary bg-primary'
              : 'text-primary'
          "
        >
          <Component :is="menu.icon" class="w-6 h-6 fill-current" />
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import StoreIcon from "../icons/store.svg";
import HomeIcon from "../icons/home.svg";
import DiscountIcon from "../icons/discount.svg";
import GraphIcon from "../icons/graph.svg";
import MessageIcon from "../icons/message.svg";
import NotificationIcon from "../icons/notification.svg";
import SettingsIcon from "../icons/settings.svg";
import LogoutIcon from "../icons/logout.svg";

const activeMenu = ref("Graph");

const menus = [
  { name: "Dashboard", icon: HomeIcon },
  { name: "Discounts", icon: DiscountIcon },
  { name: "Graph", icon: GraphIcon },
  { name: "Messages", icon: MessageIcon },
  { name: "Notifications", icon: NotificationIcon },
  { name: "Settings", icon: SettingsIcon },
  { name: "Logout", icon: LogoutIcon },
];
</script>
