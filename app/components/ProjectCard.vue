<template>
  <a 
    :href="project.vercelUrl" 
    target="_blank" 
    class="bg-slate-900 rounded-2xl border border-slate-800 overflow-hidden hover:border-emerald-500/30 hover:-translate-y-1.5 transition-all duration-300 group flex flex-col justify-between block relative"
  >
    <div class="p-6 space-y-4">
      <div class="flex justify-between items-center">
        <span :class="['text-[10px] font-mono font-bold px-2 py-0.5 rounded-md border tracking-wider uppercase', project.tagClass]">
          {{ project.tag }}
        </span>
        
        <div class="relative z-10 flex items-center space-x-2 text-slate-400">
          <a 
            :href="project.githubUrl" 
            target="_blank" 
            @click.stop
            class="hover:text-white p-1.5 hover:bg-slate-800 rounded-lg transition-all" 
            title="View Source Code"
          >
            <Icon name="mdi:github" class="w-5 h-5" />
          </a>
        </div>
      </div>
      <div class="aspect-video overflow-hidden">
        <img
          :src="project.image"
          :alt="project.title"
          class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500"
        />
      </div>
      <h3 class="text-base font-bold text-white group-hover:text-emerald-400 transition-colors leading-snug">
        {{ project.title }}
      </h3>
      <p class="text-slate-400 text-xs leading-relaxed line-clamp-4">
        {{ project.description }}
      </p>
    </div>
    
    <div class="p-6 pt-0">
      <div class="flex flex-wrap gap-1 pt-2 border-t border-slate-800/40">
        <span 
          v-for="(tech, techIndex) in project.techStack" 
          :key="techIndex"
          class="text-[10px] bg-slate-950 text-slate-300 px-2 py-0.5 rounded border border-slate-800 font-mono flex items-center gap-1"
        >
          <Icon v-if="tech === 'React'" name="simple-icons:react" class="text-sky-400 w-3 h-3" />
          <Icon v-if="tech === 'Nuxt'" name="simple-icons:nuxtdotjs" class="text-emerald-500 w-3 h-3" />
          {{ tech }}
        </span>
      </div>
    </div>
  </a>
</template>

<script setup>
defineProps({
  project: {
    type: Object,
    required: true
  }
})
</script>
