<template>
  <div class="min-h-screen bg-slate-900 text-slate-100 flex flex-col">
    
    <header 
      :class="[
        'sticky top-0 z-50 transition-all duration-300',
        isScrolled || isMenuOpen
          ? 'bg-slate-950/90 backdrop-blur-md border-b border-slate-800 shadow-xl' 
          : 'bg-transparent border-transparent'
      ]"
    >
      <nav class="max-w-6xl mx-auto px-4 h-16 flex items-center justify-between">
        <a href="#" class="text-xl font-bold bg-gradient-to-r from-green-400 to-emerald-500 bg-clip-text text-transparent">
          RYU
        </a>

        <!-- Desktop Navigation -->
        <ul class="hidden md:flex items-center space-x-6 text-sm font-medium text-slate-300">
          <li><a href="#about" class="hover:text-emerald-400 transition-colors">About Me</a></li>
          <li><a href="#skills" class="hover:text-emerald-400 transition-colors">Skills</a></li>
          <li><a href="#portfolio" class="hover:text-emerald-400 transition-colors">Portfolio</a></li>
          <li><a href="#experience" class="hover:text-emerald-400 transition-colors">Experience</a></li>
          <li><a href="#contact" class="bg-emerald-500 hover:bg-emerald-600 text-slate-950 px-4 py-2 rounded-full font-semibold transition-all">Contact Me</a></li>
        </ul>

        <!-- Mobile Menu Button -->
        <button @click="isMenuOpen = !isMenuOpen" class="md:hidden p-2 text-slate-300 hover:text-emerald-400 transition-colors focus:outline-none">
          <Icon :name="isMenuOpen ? 'mdi:close' : 'mdi:menu'" class="w-6 h-6" />
        </button>
      </nav>

      <!-- Mobile Navigation Dropdown -->
      <transition enter-active-class="transition duration-200 ease-out" enter-from-class="transform -translate-y-4 opacity-0" enter-to-class="transform translate-y-0 opacity-100" leave-active-class="transition duration-150 ease-in" leave-from-class="transform translate-y-0 opacity-100" leave-to-class="transform -translate-y-4 opacity-0">
        <div v-if="isMenuOpen" class="md:hidden border-t border-slate-800 bg-slate-950/95 backdrop-blur-lg">
          <ul class="flex flex-col p-4 space-y-4 text-sm font-medium text-slate-300">
            <li><a href="#about" @click="isMenuOpen = false" class="block py-2 hover:text-emerald-400 transition-colors">About Me</a></li>
            <li><a href="#skills" @click="isMenuOpen = false" class="block py-2 hover:text-emerald-400 transition-colors">Skills</a></li>
            <li><a href="#portfolio" @click="isMenuOpen = false" class="block py-2 hover:text-emerald-400 transition-colors">Portfolio</a></li>
            <li><a href="#experience" @click="isMenuOpen = false" class="block py-2 hover:text-emerald-400 transition-colors">Experience</a></li>
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

    <footer id="contact" class="bg-slate-950 border-t border-slate-800 pt-16 pb-6">
      <div class="max-w-xl mx-auto px-4 flex flex-col items-center text-center space-y-8">
        
        <div class="space-y-2">
          <h3 class="text-3xl font-bold text-white tracking-wide">Contact</h3>
        </div>

        <div class="flex items-center space-x-4">
          <a href="https://www.facebook.com/Ryugiz" target="_blank" class="p-3 bg-slate-900 hover:bg-emerald-500/10 rounded-xl text-slate-400 hover:text-emerald-400 border border-slate-800 transition-all" title="Facebook">
            <Icon name="mdi:facebook" class="w-6 h-6" />
          </a>
          <a href="https://www.instagram.com/ryxvibe/" target="_blank" class="p-3 bg-slate-900 hover:bg-emerald-500/10 rounded-xl text-slate-400 hover:text-emerald-400 border border-slate-800 transition-all" title="Instagram">
            <Icon name="mdi:instagram" class="w-6 h-6" />
          </a>
          <a href="https://github.com/ryugxz" target="_blank" class="p-3 bg-slate-900 hover:bg-emerald-500/10 rounded-xl text-slate-400 hover:text-emerald-400 border border-slate-800 transition-all" title="GitHub">
            <Icon name="mdi:github" class="w-6 h-6" />
          </a>
        </div>

        <div class="w-full space-y-3 max-w-sm">
          <div class="flex items-center justify-between bg-slate-900/60 border border-slate-800 px-4 py-3 rounded-xl group">
            <div class="flex items-center space-x-3 text-slate-300">
              <Icon name="mdi:email-outline" class="w-5 h-5 text-emerald-400" />
              <span class="text-sm font-mono select-all">ryxgxz@gmail.com</span>
            </div>
            <button @click="copyToClipboard('ryxgxz@gmail.com', 'email')" class="text-xs bg-slate-800 hover:bg-emerald-500 hover:text-slate-950 text-slate-400 px-2.5 py-1 rounded-md transition-all active:scale-95">
              {{ copiedType === 'email' ? 'Copied!' : 'Copy' }}
            </button>
          </div>

          <div class="flex items-center justify-between bg-slate-900/60 border border-slate-800 px-4 py-3 rounded-xl group">
            <div class="flex items-center space-x-3 text-slate-300">
              <Icon name="mdi:phone-outline" class="w-5 h-5 text-emerald-400" />
              <span class="text-sm font-mono select-all">0967564318</span>
            </div>
            <button @click="copyToClipboard('0967564318', 'phone')" class="text-xs bg-slate-800 hover:bg-emerald-500 hover:text-slate-950 text-slate-400 px-2.5 py-1 rounded-md transition-all active:scale-95">
              {{ copiedType === 'phone' ? 'Copied!' : 'Copy' }}
            </button>
          </div>
        </div>

        <div class="pt-2">
          <a href="#" class="text-xs text-slate-500 hover:text-emerald-400 flex items-center space-x-1 transition-colors mx-auto">
            <span>Back to top</span>
            <Icon name="mdi:arrow-up" class="w-4 h-4" />
          </a>
        </div>

        <div class="w-full pt-8 border-t border-slate-900 text-xs text-slate-600">
          <p>© {{ new Date().getFullYear() }} • Credit by ratipong. All rights reserved.</p>
        </div>
      </div>
    </footer>

  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import { useHead } from '#imports'

// กำหนดให้แท็ก html มีคุณสมบัติ scroll-smooth เพื่อให้การเลื่อนหน้าจอผ่าน Anchor Links นุ่มนวลขึ้น
useHead({
  htmlAttrs: {
    class: 'scroll-smooth'
  }
})

// State สำหรับควบคุมการเปิด/ปิดเมนูบน Mobile
const isMenuOpen = ref(false)

// จัดการการเปลี่ยนสี Header เมื่อมีการ Scroll
const isScrolled = ref(false)
const handleScroll = () => {
  isScrolled.value = window.scrollY > 20
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
  handleScroll() // ตรวจสอบสถานะทันทีเมื่อโหลดหน้า (กรณี Refresh หน้าจอขณะไม่ได้อยู่ด้านบนสุด)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})

// ตัวแปรไว้เช็คสเตตัสว่ากำลังคัดลอกอันไหนอยู่ เพื่อเปลี่ยนข้อความปุ่มเป็น "Copied!" ชั่วคราว
const copiedType = ref(null)

const copyToClipboard = (text, type) => {
  navigator.clipboard.writeText(text).then(() => {
    copiedType.value = type
    // หลังจาก 2 วินาที ให้เปลี่ยนข้อความปุ่มกลับมาเป็น "Copy" เหมือนเดิม
    setTimeout(() => {
      copiedType.value = null
    }, 2000)
  }).catch(err => {
    console.error('Failed to copy text: ', err)
  })
}
</script>