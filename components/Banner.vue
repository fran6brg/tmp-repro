<script setup lang="ts">
import { appDebug } from '../constants/index'
</script>

<template>
  <div class="w-full flex justify-center items-center gap-3 px-3 backdrop-filter backdrop-blur" :class="{ 'bg-white dark:bg-black': appDebug }">
    <p class="text-xs">
      wip
    </p>
  </div>
</template>
