<!-- eslint-disable vue/multi-word-component-names -->
<script setup lang="ts">
const props = defineProps<{
  multiplier: number
}>()
const count = ref(12)
const doubled = computed(() => count.value * props.multiplier)
</script>

<template>
  <div class="sugar-counter">
    Sugar Counter {{ count }} x {{ multiplier }} = {{ doubled }}
    <button @click="count += 1">
      Inc
    </button>
  </div>
</template>
