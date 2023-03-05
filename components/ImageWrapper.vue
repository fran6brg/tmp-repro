<script setup lang="ts">
import { sizes } from '../constants/index'

/**
 * props
 */

defineProps({
  source: {
    type: String as () => string,
    required: false,
    default: null,
  },
  shape: {
    type: String as () => string,
    required: false,
    default: 'square',
    validator: (x: string) => ['square', 'rounded', 'squircle'].includes(x),
  },
  size: {
    type: String,
    required: false,
    default: 'xs',
    validator: (x: string) => sizes.includes(x),
  },
})
</script>

<template>
  <div
    class="flex items-center justify-center wsc-transition-all transform hover:scale-105"
    :class="{
      'h-6 w-6 min-w-6': size === sizes[0],
      'h-10 w-10 min-w-10': size === sizes[1],
      'h-14 w-14 min-w-14': size === sizes[2],
      'h-20 w-20 min-w-20': size === sizes[3],
      'h-28 w-28 min-w-28': size === sizes[4],
      'h-36 w-36 min-w-36': size === sizes[5],
    }"
  >
    <ClientOnly>
      <img
        v-if="source"
        :src="source"
        class="h-full object-cover"
        :class="{
          'rounded-full': shape === 'rounded',
          'rounded-md': shape === 'squircle',
        }"
      >
      <div v-else class="h-full w-full fake-line rounded-full" />
    </ClientOnly>
  </div>
</template>
