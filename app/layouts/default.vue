<template>
  <div class="min-h-screen bg-slate-900 text-slate-100 flex flex-col font-sans selection:bg-emerald-500/30 selection:text-emerald-300">
    
    <header 
      :class="[
        'sticky top-0 z-50 transition-all duration-300',
        isScrolled || isMenuOpen
          ? 'bg-slate-950/90 backdrop-blur-md border-b border-slate-800/80 shadow-2xl shadow-slate-950/20' 
          : 'bg-transparent border-transparent'
      ]"
    >
      <nav class="max-w-6xl mx-auto px-4 h-16 flex items-center justify-between">
        <a href="#" class="text-xl font-mono font-bold bg-gradient-to-r from-emerald-400 to-teal-400 bg-clip-text text-transparent hover:scale-105 transition-transform">
          RYU.DEV
        </a>

        <ul class="hidden md:flex items-center space-x-1 text-sm font-medium text-slate-300">
          <li><a href="https://github.com/ryugxz" target="_blank" class="p-2 rounded-xl hover:text-emerald-400 hover:bg-slate-800/40 transition-colors"> <Icon name="mdi:github" /></a></li>
          <li><a href="#about" class="px-4 py-2 rounded-xl hover:text-emerald-400 hover:bg-slate-800/50 transition-all">About Me</a></li>
          <li><a href="#skills" class="px-4 py-2 rounded-xl hover:text-emerald-400 hover:bg-slate-800/50 transition-all">Skills</a></li>
          <li><a href="#portfolio" class="px-4 py-2 rounded-xl hover:text-emerald-400 hover:bg-slate-800/50 transition-all">Portfolio</a></li>
          <li><a href="#experience" class="px-4 py-2 rounded-xl hover:text-emerald-400 hover:bg-slate-800/50 transition-all">Experience</a></li>
          <li class="pl-4">
            <a href="#contact" class="bg-emerald-500 hover:bg-emerald-600 active:scale-95 text-slate-950 px-5 py-2.5 rounded-xl font-bold transition-all shadow-md shadow-emerald-500/10 hover:shadow-emerald-500/20">
              Contact Me
            </a>
          </li>
        </ul>

        <button 
          @click="isMenuOpen = !isMenuOpen" 
          class="md:hidden p-2 text-slate-300 hover:text-emerald-400 hover:bg-slate-800/40 rounded-xl transition-colors focus:outline-none"
          aria-label="Toggle Navigation Menu"
        >
          <Icon :name="isMenuOpen ? 'mdi:close' : 'mdi:menu'" class="w-6 h-6" />
        </button>
      </nav>

      <transition 
        enter-active-class="transition duration-200 ease-out" 
        enter-from-class="transform -translate-y-4 opacity-0" 
        enter-to-class="transform translate-y-0 opacity-100" 
        leave-active-class="transition duration-150 ease-in" 
        leave-from-class="transform translate-y-0 opacity-100" 
        leave-to-class="transform -translate-y-4 opacity-0"
      >
        <div v-if="isMenuOpen" class="md:hidden border-t border-slate-800 bg-slate-950/95 backdrop-blur-lg absolute w-full left-0 shadow-2xl">
          <ul class="flex flex-col p-4 space-y-2 text-sm font-medium text-slate-300">
            <li><a href="#about" @click="isMenuOpen = false" class="flex items-center gap-3 px-4 py-3 rounded-xl hover:bg-slate-900 hover:text-emerald-400 transition-colors">About Me</a></li>
            <li><a href="#skills" @click="isMenuOpen = false" class="flex items-center gap-3 px-4 py-3 rounded-xl hover:bg-slate-900 hover:text-emerald-400 transition-colors">Skills</a></li>
            <li><a href="#portfolio" @click="isMenuOpen = false" class="flex items-center gap-3 px-4 py-3 rounded-xl hover:bg-slate-900 hover:text-emerald-400 transition-colors">Portfolio</a></li>
            <li><a href="#experience" @click="isMenuOpen = false" class="flex items-center gap-3 px-4 py-3 rounded-xl hover:bg-slate-900 hover:text-emerald-400 transition-colors">Experience</a></li>
            <li class="pt-2">
              <a href="#contact" @click="isMenuOpen = false" class="block bg-emerald-500 hover:bg-emerald-600 text-slate-950 px-4 py-3 rounded-xl font-bold text-center transition-all shadow-lg shadow-emerald-500/10">
                Contact Me
              </a>
            </li>
          </ul>
        </div>
      </transition>
    </header>

    <main class="flex-grow">
      <slot />
    </main>

    <footer id="contact" class="bg-slate-950 border-t border-slate-800 pt-20 pb-8">
      <div class="max-w-xl mx-auto px-4 flex flex-col items-center text-center space-y-10">
        
        <div class="space-y-2">
          <h3 class="text-3xl font-bold text-white tracking-wide">Get In Touch</h3>
          <p class="text-slate-400 text-sm">พร้อมที่จะร่วมงานหรือแลกเปลี่ยนโปรเจกต์ไอเดียดีๆ ติดต่อเข้ามาได้เลยครับ</p>
        </div>

        <div class="flex items-center space-x-4">
          <a href="https://www.facebook.com/Ryugiz" target="_blank" class="p-3 bg-slate-900 hover:bg-emerald-500/10 rounded-xl text-slate-400 hover:text-emerald-400 border border-slate-800 hover:border-emerald-500/30 transition-all hover:-translate-y-0.5" title="Facebook">
            <Icon name="mdi:facebook" class="w-6 h-6" />
          </a>
          <a href="https://www.instagram.com/ryxvibe/" target="_blank" class="p-3 bg-slate-900 hover:bg-emerald-500/10 rounded-xl text-slate-400 hover:text-emerald-400 border border-slate-800 hover:border-emerald-500/30 transition-all hover:-translate-y-0.5" title="Instagram">
            <Icon name="mdi:instagram" class="w-6 h-6" />
          </a>
          <a href="https://github.com/ryugxz" target="_blank" class="p-3 bg-slate-900 hover:bg-emerald-500/10 rounded-xl text-slate-400 hover:text-emerald-400 border border-slate-800 hover:border-emerald-500/30 transition-all hover:-translate-y-0.5" title="GitHub">
            <Icon name="mdi:github" class="w-6 h-6" />
          </a>
        </div>

        <div class="w-full space-y-3 max-w-sm">
          <div class="flex items-center justify-between bg-slate-900/40 border border-slate-800/80 px-4 py-3 rounded-xl group hover:border-slate-700 transition-colors">
            <div class="flex items-center space-x-3 text-slate-300">
              <Icon name="mdi:email-outline" class="w-5 h-5 text-emerald-400" />
              <span class="text-sm font-mono select-all">ryxgxz@gmail.com</span>
            </div>
            <button @click="copyToClipboard('ryxgxz@gmail.com', 'email')" class="text-xs bg-slate-800 hover:bg-emerald-500 hover:text-slate-950 text-slate-400 px-3 py-1.5 rounded-lg font-medium transition-all active:scale-95">
              {{ copiedType === 'email' ? 'Copied!' : 'Copy' }}
            </button>
          </div>

          <div class="flex items-center justify-between bg-slate-900/40 border border-slate-800/80 px-4 py-3 rounded-xl group hover:border-slate-700 transition-colors">
            <div class="flex items-center space-x-3 text-slate-300">
              <Icon name="mdi:phone-outline" class="w-5 h-5 text-emerald-400" />
              <span class="text-sm font-mono select-all">0967564318</span>
            </div>
            <button @click="copyToClipboard('0967564318', 'phone')" class="text-xs bg-slate-800 hover:bg-emerald-500 hover:text-slate-950 text-slate-400 px-3 py-1.5 rounded-lg font-medium transition-all active:scale-95">
              {{ copiedType === 'phone' ? 'Copied!' : 'Copy' }}
            </button>
          </div>
        </div>

        <div class="pt-4">
          <a href="#" class="text-xs text-slate-500 hover:text-emerald-400 flex items-center space-x-1 transition-colors mx-auto group">
            <span>Back to top</span>
            <Icon name="mdi:arrow-up" class="w-4 h-4 group-hover:-translate-y-0.5 transition-transform" />
          </a>
        </div>

        <div class="w-full pt-8 border-t border-slate-900 text-xs text-slate-600 font-mono">
          <p>© {{ new Date().getFullYear() }} • Crafted with Passion by Ratipong. All rights reserved.</p>
        </div>
      </div>
    </footer>

  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import { useHead } from '#imports'

useHead({
  htmlAttrs: {
    class: 'scroll-smooth',
    style: 'scroll-padding-top: 4rem;'
  }
})

const isMenuOpen = ref(false)
const isScrolled = ref(false)

const handleScroll = () => {
  if (typeof window !== 'undefined') {
    isScrolled.value = window.scrollY > 20
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
  handleScroll()
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})

const copiedType = ref(null)

const copyToClipboard = (text, type) => {
  navigator.clipboard.writeText(text).then(() => {
    copiedType.value = type
    setTimeout(() => {
      copiedType.value = null
    }, 2000)
  }).catch(err => {
    console.error('Failed to copy text: ', err)
  })
}
</script>