<script setup lang="ts">
import { appDebug } from '../constants/index'
import * as packageJson from '../package.json'
</script>

<template>
  <div class="w-full p-3 flex justify-between gap-3 backdrop-filter backdrop-blur" :class="{ 'bg-gray-100 dark:bg-gray-900': appDebug }">
    <p>Version: {{ packageJson.version }}</p>
    <NuxtLink i-carbon-campsite to="https://fran6.eth.limo" target="_blank" rel="noopener">
      IPFS hosted
    </NuxtLink>
  </div>
</template>
