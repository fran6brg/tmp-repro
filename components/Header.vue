<script setup lang="ts">
import { appDebug } from '../constants/index'
</script>

<template>
  <div class="w-full flex justify-between items-center gap-3 px-3 backdrop-filter backdrop-blur" :class="{ 'bg-gray-100 dark:bg-gray-900': appDebug }">
    <div class="flex items-center gap-2">
      <ImageWrapper
        source="https://pbs.twimg.com/profile_images/1628705902365736965/wtKU249l_400x400.jpg"
        shape="rounded"
        size="xs"
      />
      <p>fran6.eth</p>
    </div>
    <DarkToggle />
  </div>
</template>
