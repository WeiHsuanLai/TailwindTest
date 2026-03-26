<script setup lang="ts">

const features = [
  {
    title: 'Vue 3 驅動',
    description: '使用最新的 Composition API，提供極速的開發體驗與執行效能。',
    icon: `<svg class="w-6 h-6 text-emerald-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/></svg>`
  },
  {
    title: 'Tailwind CSS v4',
    description: '全新的引擎，極簡的設定，讓樣式開發比以往任何時候都更快。',
    icon: `<svg class="w-6 h-6 text-sky-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 5a1 1 0 011-1h14a1 1 0 011 1v2a1 1 0 01-1 1H5a1 1 0 01-1-1V5zM4 13a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H5a1 1 0 01-1-1v-6zM16 13a1 1 0 011-1h2a1 1 0 011 1v6a1 1 0 01-1 1h-2a1 1 0 01-1-1v-6z"/></svg>`
  },
  {
    title: '現代化架構',
    description: '整合 Vite 7、TypeScript 與 Pinia，打造企業級的前端應用基礎。',
    icon: `<svg class="w-6 h-6 text-indigo-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"/></svg>`
  }
]
</script>

<template>
  <div class="min-h-screen bg-slate-50 font-sans text-slate-900 selection:bg-indigo-100 selection:text-indigo-700">
    <!-- Navigation -->
    <nav class="sticky top-0 z-50 bg-white/80 backdrop-blur-md border-b border-slate-200">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between h-16 items-center">
          <div class="flex items-center gap-2">
            <div class="w-8 h-8 bg-indigo-600 rounded-lg flex items-center justify-center">
              <span class="text-white font-bold text-xl">V</span>
            </div>
            <span class="text-xl font-bold bg-clip-text text-transparent bg-linear-to-r from-indigo-600 to-sky-500">
              ViteVue
            </span>
          </div>
          <div class="hidden md:flex items-center space-x-8 text-sm font-medium text-slate-600">
            <a href="#" class="hover:text-indigo-600 transition-colors">產品介紹</a>
            <a href="#" class="hover:text-indigo-600 transition-colors">技術文件</a>
            <a href="#" class="hover:text-indigo-600 transition-colors">社群支援</a>
            <button class="bg-slate-900 text-white px-5 py-2 rounded-full hover:bg-slate-800 transition-all transform hover:scale-105 active:scale-95">
              立即開始
            </button>
          </div>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <header class="relative overflow-hidden pt-16 pb-24 lg:pt-32 lg:pb-40">
      <!-- Background Decorations -->
      <div class="absolute top-0 left-1/2 -translate-x-1/2 w-full h-full -z-10">
        <div class="absolute top-[-10%] left-[-10%] w-[40%] h-[40%] bg-indigo-200/40 rounded-full blur-3xl"></div>
        <div class="absolute bottom-0 right-[-5%] w-[30%] h-[30%] bg-sky-200/30 rounded-full blur-3xl"></div>
      </div>

      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h1 class="text-5xl lg:text-7xl font-extrabold tracking-tight mb-8">
          打造下一個 <br />
          <span class="text-indigo-600">驚艷世界</span> 的網頁
        </h1>
        <p class="max-w-2xl mx-auto text-lg lg:text-xl text-slate-600 mb-12 leading-relaxed">
          透過 Vue 3 的高效能元件架構與 Tailwind CSS v4 的強大樣式系統，
          讓您的創意不再受限於技術開發，專注於提供極致的使用者體驗。
        </p>
        <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
          <button class="w-full sm:w-auto px-8 py-4 bg-indigo-600 text-white rounded-2xl font-bold text-lg hover:bg-indigo-700 shadow-lg shadow-indigo-200 transition-all transform hover:-translate-y-1">
            免費開始體驗
          </button>
          <button class="w-full sm:w-auto px-8 py-4 bg-white text-slate-700 border border-slate-200 rounded-2xl font-bold text-lg hover:bg-slate-50 transition-all">
            觀看展示影片
          </button>
        </div>
      </div>
    </header>

    <!-- Features Section -->
    <section class="py-24 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-3xl font-bold text-slate-900 mb-4">為什麼選擇我們的架構？</h2>
          <div class="h-1.5 w-20 bg-indigo-600 mx-auto rounded-full"></div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div v-for="feature in features" :key="feature.title"
               class="p-8 rounded-3xl border border-slate-100 bg-slate-50/50 hover:bg-white hover:shadow-2xl hover:shadow-indigo-50 transition-all group">
            <div class="w-12 h-12 rounded-2xl bg-white shadow-sm flex items-center justify-center mb-6 group-hover:scale-110 transition-transform"
                 v-html="feature.icon">
            </div>
            <h3 class="text-xl font-bold mb-4 text-slate-900">{{ feature.title }}</h3>
            <p class="text-slate-600 leading-relaxed text-sm lg:text-base">
              {{ feature.description }}
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="bg-slate-900 text-slate-400 py-12">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center text-sm">
        <p>© 2026 ViteVue Project. Built with ❤️ and Tailwind CSS v4.</p>
      </div>
    </footer>
  </div>
</template>

<style scoped>
/* 使用 Tailwind v4 的 CSS 變數或自定義類別 (選用) */
</style>
