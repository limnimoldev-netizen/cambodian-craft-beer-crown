<template>
  <header class="sticky top-0 z-50 bg-white border-b border-gray-100 shadow-sm">
    <div class="max-w-[1280px] mx-auto px-6 md:px-12">
      <div class="flex h-20 items-center justify-between">
        
        <div class="flex items-center">
          <img src="@/assets/ourlogo.png" alt="Cambodian Beer Crown 2026" class="h-14 w-auto object-contain" />
        </div>

        <nav class="hidden md:flex items-center gap-8 font-medium text-base">
          <RouterLink 
            to="/home" 
            class="text-[#333333] hover:text-[#f0a22a] pb-1 transition-colors relative"
            active-class="border-b-2 border-[#f0a22a] text-black font-semibold"
          >
            Home
          </RouterLink>

          <RouterLink 
            to="/breweries" 
            class="text-[#333333] hover:text-[#f0a22a] pb-1 transition-colors"
            active-class="border-b-2 border-[#f0a22a] text-black font-semibold"
          >
            Breweries
          </RouterLink>

          <RouterLink 
            to="/schedule" 
            class="text-[#333333] hover:text-[#f0a22a] pb-1 transition-colors"
            active-class="border-b-2 border-[#f0a22a] text-black font-semibold"
          >
            Schedule
          </RouterLink>

          <RouterLink 
            to="/styles" 
            class="text-[#333333] hover:text-[#f0a22a] pb-1 transition-colors"
            active-class="border-b-2 border-[#f0a22a] text-black font-semibold"
          >
            Styles
          </RouterLink>

          <RouterLink 
            to="/awards" 
            class="text-[#333333] hover:text-[#f0a22a] pb-1 transition-colors"
            active-class="border-b-2 border-[#f0a22a] text-black font-semibold"
          >
            Awards
          </RouterLink>

          <RouterLink 
            to="/sponsors" 
            class="text-[#333333] hover:text-[#f0a22a] pb-1 transition-colors"
            active-class="border-b-2 border-[#f0a22a] text-black font-semibold"
          >
            Sponsors
          </RouterLink>
        </nav>

        <div>
          <RouterLink 
            to="/judge" 
            class="inline-flex items-center bg-[#f0a22a] hover:bg-[#e09119] text-white px-5 py-2.5 rounded-full font-semibold transition-all shadow-sm text-sm tracking-wide"
          >
            <svg class="w-4 h-4 mr-1.5" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z"></path>
            </svg>
            Judge here
          </RouterLink>
        </div>

      </div>
    </div>
  </header>
</template>