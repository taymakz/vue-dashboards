<script setup lang="ts">
import type { HTMLAttributes } from 'vue'
import { cn } from '@/utils/cn'

const props = defineProps<{
  class?: HTMLAttributes['class']
}>()
</script>

<template>
  <div
    data-slot="alert-dialog-header"
    :class="cn('flex flex-col gap-2 text-center sm:text-right', props.class)"
  >
    <slot />
  </div>
</template>
