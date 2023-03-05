<template>
  <div class="page-wrapper">
    <slot />
  </div>
</template>

<style scoped>
.page-wrapper {
 @apply w-full h-full;
 /* @apply min-w-xs max-w-160; */
 @apply flex flex-col mx-auto;
 @apply overflow-x-auto overflow-y-auto;
 @apply flex justify-center items-center;

 /* debug */
 /* @apply border-1 border-red-500; */
}
</style>
