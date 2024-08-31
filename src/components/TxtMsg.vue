<script lang="ts" setup>
const props = defineProps({
  left: {
    type: Boolean,
    default: false,
  },
})
</script>

<template>
  <div v-if="props.left" class="flex justify-start mb-4">
    <div class="bg-gray-300 text-black p-3 rounded-lg max-w-md">
      <slot />
    </div>
  </div>
  <div v-else class="flex justify-end mb-4">
    <div class="bg-blue-500 text-white p-3 rounded-lg max-w-md">
      <slot />
    </div>
  </div>
</template>
