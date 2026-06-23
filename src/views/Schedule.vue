<template>
  <section class="pt-7 bg-[#FAF9F5] min-h-screen">
    <div class="mx-auto max-w-5xl">
      <div class="mx-auto max-w-2xl bg-[#FAF9F5] flex flex-col">
        
        <!-- Main Content -->
        <main class="max-w-2xl mx-auto w-full px-6 pb-5">
          
          <!-- Header with Animations -->
          <p class="text-amber-500 font-medium animate-fade-in-up">Event Day</p>
          <h1 class="text-3xl font-bold text-gray-900 sm:text-4xl animate-fade-in-up" style="animation-delay: 0.1s;">Schedule</h1>
          <div class="w-33 h-[2px] bg-[#EE9F27] animate-scale-x" style="animation-delay: 0.2s;"></div>
          
          <!-- Description -->
          <p class="text-gray-600 mb-9 mt-7 animate-fade-in-up" style="animation-delay: 0.3s;">
            The full schedule will be confirmed 2–3 weeks before the event. Join us for an evening of craft beer tasting, food pairing, brewery stories, and networking with fellow beer enthusiasts. Explore unique flavors and discover the art of Cambodian craft brewing.
          </p>

          <!-- Schedule Items -->
          <div class="flex flex-col gap-0">
            <div 
              v-for="(item, index) in schedules" 
              :key="index"
              class="border-b border-amber-500 pb-4 mb-4 animate-fade-in-up"
              :style="{ animationDelay: (0.1 * (index + 1)) + 's' }"
            >
              <!-- Time + Event -->
              <div class="flex items-center gap-6 mb-1">
                <span class="text-amber-600 font-semibold text-lg w-24">
                  {{ item.time }}
                </span>
                <span class="text-amber-500 text-xl">•</span>
                <span class="text-gray-900 font-medium text-lg">
                  {{ item.title }}
                </span>
              </div>
              <!-- Sub description -->
              <p class="text-gray-900 text-sm ml-0">{{ item.desc }}</p>
            </div>
          </div>

        </main>

      </div>
    </div>
  </section>
</template>

<script setup>
const schedules = [
  {
    time: '2 : 00 PM',
    title: 'Event Begins',
    desc: 'Guest arrive, collect tasted product',
  },
  {
    time: '3 : 15 PM',
    title: 'Introduction by the MC',
    desc: 'Brief presentation about the brewery, brewing process, and today',
  },
  {
    time: '3 : 30 PM',
    title: 'DJ Wha-wah (Until 6:30)',
    desc: 'Guest arrive, collect tasted product',
  },
  {
    time: '6 : 40 PM',
    title: 'Blind Tasting live session',
    desc: 'Guest arrive, collect tasted product',
  },
  {
    time: '7 : 30 PM',
    title: 'Start award ceremony',
    desc: 'Guest arrive, collect tasted product',
  },
  {
    time: '8 : 30 PM',
    title: 'Live music by the broken cymbal (until 11:00pm)',
    desc: 'Guest arrive, collect tasted product',
  },
  {
    time: '11 : 30 PM',
    title: 'Event Ends',
    desc: 'Guest arrive, collect tasted product',
  },
]
</script>

<style scoped>
/* Simple Animations */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes scaleX {
  from {
    transform: scaleX(0);
  }
  to {
    transform: scaleX(1);
  }
}

.animate-fade-in-up {
  opacity: 0;
  animation: fadeInUp 0.6s ease-out forwards;
}

.animate-scale-x {
  animation: scaleX 0.6s ease-out forwards;
  transform-origin: left;
}

/* Optional hover effect for schedule items */
.border-b {
  transition: background-color 0.2s ease, padding-left 0.2s ease;
  cursor: default;
}

.border-b:hover {
  background-color: #fdf6ee;
  padding-left: 8px;
  border-radius: 8px;
}
</style>