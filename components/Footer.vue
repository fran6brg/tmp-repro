<script setup lang="ts">
import { appDebug } from '../constants/index'
</script>

<template>
  <div class="w-full p-3 flex justify-end gap-3 backdrop-filter backdrop-blur" :class="{ 'bg-gray-100 dark:bg-gray-900': appDebug }">
    <NuxtLink i-carbon-campsite to="https://fran6.eth.limo" target="_blank" rel="noopener">
      IPFS hosted
    </NuxtLink>
  </div>
</template>
