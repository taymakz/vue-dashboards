<script setup lang="ts">
import type { HTMLAttributes } from 'vue'


const props = defineProps<{
  class?: HTMLAttributes['class']
}>()
</script>

<template>
  <div
    data-slot="dialog-header"
    :class="cn('flex flex-col gap-2 text-center sm:text-right', props.class)"
  >
    <slot />
  </div>
</template>
