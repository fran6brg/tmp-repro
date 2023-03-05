<script setup lang="ts">
const online = useOnline()
</script>

<template>
  <div class="overflow-y-scroll w-full">
    <Suspense>
      <ClientOnly>
        <div v-if="!online" text-gray:80>
          You're offline
        </div>
      </ClientOnly>
      <template #fallback>
        <div op50 italic>
          <span animate-pulse>Loading...</span>
        </div>
      </template>
    </Suspense>
    <div v-for="i in 10" :key="i" class="w-full h-25 bg-white dark:bg-black">
      scroll mf
    </div>
  </div>
</template>
