<template>
  <div class="flex bg-[#7b2a26] text-[#fffbee] py-5 justify-between">
    <div class="flex justify-start flex-wrap">
      <div
        v-for="header in headers"
        :key="header"
        class="ml-10 px-6 py-2 hover:bg-[#4d1311]"
      >
        {{ header }}
      </div>
    </div>
    <div class="flex right-10 px-6 py-2 hover:bg-[#4d1311] items-center">
      <!-- <div class="absolute right-10 px-6 py-2 hover:bg-[#4d1311]"> -->
      <svg
        aria-hidden="true"
        class="w-5 h-5 text-[#fffbee]"
        fill="none"
        stroke="currentColor"
        viewBox="0 0 24 24"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
        ></path>
      </svg>
    </div>
  </div>
</template>
<script setup lang="ts">
import { ref } from "@vue/runtime-core";

const headers = ref([
  "Home",
  "Manufacturing",
  "Sales",
  "Rental",
  "Careers",
  "Contact Us",
]);
</script>
