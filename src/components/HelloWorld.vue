<script setup lang="ts">
import { Button } from '@/components/ui/button'
defineProps<{ msg: string }>()

</script>

<template>
  <h1>{{ msg }}</h1>
  <Button>Ok</Button>

</template>

<style scoped>
</style>
