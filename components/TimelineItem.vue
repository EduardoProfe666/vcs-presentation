<script setup lang="ts">
defineProps({
  date: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="timeline-item">
    <div class="timeline-date">{{ date }}</div>
    <div class="timeline-content">
      <div class="info-block">
        <h3 class="text-lg font-bold">{{ title }}</h3>
        <p class="mt-2 text-sm opacity-80">{{ description }}</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.timeline-item {
  @apply flex items-start gap-4 my-4 relative pl-6;
}

.timeline-date {
  @apply text-sm font-mono opacity-75 min-w-[80px];
}

.timeline-content {
  @apply flex-1;
}

.timeline-item::before {
  content: '';
  @apply absolute left-0 top-2 w-2 h-2 rounded-full bg-blue-400;
}

.timeline-item::after {
  content: '';
  @apply absolute left-[3px] top-4 w-[2px] h-full bg-blue-400/30;
}

.timeline-item:last-child::after {
  display: none;
}
</style>