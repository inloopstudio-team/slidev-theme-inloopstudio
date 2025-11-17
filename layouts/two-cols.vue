<script setup lang="ts">
import BrandHeader from '../components/BrandHeader.vue'

const props = defineProps({
  class: {
    type: String,
  },
  layoutClass: {
    type: String,
  },
})
</script>

<template>
  <div class="slidev-layout two-columns inloop-bg w-full h-full grid grid-cols-2 gap-4 px-16 py-8 pt-24" :class="props.layoutClass">
    <BrandHeader />
    <div class="col-left pr-4" :class="props.class">
      <slot />
    </div>
    <div class="col-right pl-4" :class="props.class">
      <slot name="right" />
    </div>
  </div>
</template>
