<script lang="ts" setup>
import type { DrawerTitleProps } from 'vaul-vue'
import type { HtmlHTMLAttributes } from 'vue'
import { DrawerTitle } from 'vaul-vue'
import { computed } from 'vue'
import { cn } from '@/utils/cn'

const props = defineProps<
  DrawerTitleProps & { class?: HtmlHTMLAttributes['class'] }
>()

const delegatedProps = computed(() => {
  const { class: _, ...delegated } = props

  return delegated
})
</script>

<template>
  <DrawerTitle
    data-slot="drawer-title"
    v-bind="delegatedProps"
    :class="cn('text-sm leading-none', props.class)"
  >
    <slot />
  </DrawerTitle>
</template>
