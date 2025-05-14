<script setup lang="ts">
import { ref, onMounted } from 'vue'

const props = defineProps({
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  },
  icon: {
    type: String,
    required: true
  }
})

const isVisible = ref(false)

onMounted(() => {
  setTimeout(() => {
    isVisible.value = true
  }, 200)
})
</script>

<template>
  <div
      class="feature-card transform transition-all duration-500"
      :class="{ 'translate-y-0 opacity-100': isVisible, 'translate-y-4 opacity-0': !isVisible }"
  >
    <div class="text-center mb-4">
      <div class="text-4xl mb-2">
        <i :class="icon"></i>
      </div>
      <h3 class="text-xl font-bold">{{ title }}</h3>
      <p class="text-sm opacity-75">{{ description }}</p>
    </div>
  </div>
</template>

<style scoped>
.feature-card {
  @apply p-6 rounded-xl bg-white/10 backdrop-blur-sm hover:bg-white/20 transition-all duration-300;
}
</style>