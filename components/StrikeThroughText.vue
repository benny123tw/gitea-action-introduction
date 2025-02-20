<script setup lang="ts">
defineProps({
  animate: {
    type: Boolean,
    default: true,
  },
  // Animation parameters for the v-motion directive
  initialAnimation: {
    type: Object,
    default: () => ({ width: '0%' }),
  },
  clickAnimation: {
    type: Object,
    default: () => ({ width: '100%', transition: { duration: 500 } }),
  },
  // Additional classes can be passed if needed
  additionalClasses: {
    type: String,
    default: '',
  },
})
</script>

<template>
  <span class="relative inline-block group">
    <slot />
    <span
      v-if="animate"
      v-motion
      :initial="initialAnimation"
      :click-1="clickAnimation"
      class="absolute left-0 top-1/2 h-[0.3rem] bg-gray-500 transform -translate-y-1/2" :class="[additionalClasses]"
    />
    <span
      v-else
      class="absolute left-0 top-1/2 h-[0.3rem] bg-gray-500 transform -translate-y-1/2 w-full" :class="[additionalClasses]"
    />
  </span>
</template>
