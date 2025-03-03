<script setup lang="ts">
import { Icon } from '@iconify/vue'
import { useColorMode } from '@vueuse/core'
import Button from './ui/button/Button.vue';


// Aktifkan color mode dari VueUse
const mode = useColorMode()
</script>

<template>
  <Button variant="ghost" @click="mode = mode === 'light' ? 'dark' : 'light'">
    <Icon
      v-if="mode === 'light'"
      icon="radix-icons:moon"
      class="h-[1.2rem] w-[1.2rem] rotate-0 scale-100 transition-all"
    />
    <Icon
      v-else
      icon="radix-icons:sun"
      class="h-[1.2rem] w-[1.2rem] rotate-90 scale-100 transition-all"
    />
  </Button>
</template>
