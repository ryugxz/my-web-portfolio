<template>
  <div :class="['bg-slate-900 border p-3 rounded-xl flex items-center space-x-3 transition-colors', isLearning ? 'border-dashed border-slate-800 hover:border-amber-500/30 group' : 'border-slate-800 hover:border-slate-700']">
    <Icon :name="icon" :class="['w-5 h-5 flex-shrink-0', isLearning ? 'grayscale group-hover:grayscale-0 transition-all' : color]" />
    <span :class="['text-sm font-medium', isLearning ? 'text-slate-400 group-hover:text-slate-200 transition-colors' : 'text-slate-200']">{{ name }}</span>
  </div>
</template>

<script setup>
defineProps({
  name: { type: String, required: true },
  icon: { type: String, required: true },
  color: { type: String, default: 'text-slate-400' },
  isLearning: { type: Boolean, default: false }
});
</script>