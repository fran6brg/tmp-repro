<script setup lang="ts">
import { appDebug } from '../constants/index'
</script>

<template>
  <main class="w-screen h-screen flex flex-col p-0 text-center relative" :class="{ 'bg-gray-100 dark:bg-gray-900': appDebug }">
    <Banner class="fixed top-0 h-8" />
    <Header class="fixed top-8 h-14" />
    <PageWrapper class="fixed mt-22">
      <div class="h-full w-full overflow-auto gap-4">
        <slot />
      </div>
    </PageWrapper>
    <Footer class="fixed bottom-0" />
  </main>
</template>
