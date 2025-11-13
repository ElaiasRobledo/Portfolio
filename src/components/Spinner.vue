<template>
  <div
    v-if="visible"
    class="fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"
  >
    <div
      class="w-12 h-12 border-4 border-t-transparent border-primary rounded-full animate-spin"
    ></div>
  </div>
</template>

<script setup>
defineProps({
  visible: { type: Boolean, default: false },
});
</script>
