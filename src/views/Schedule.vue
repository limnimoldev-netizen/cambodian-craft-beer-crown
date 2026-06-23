<template>
   <section class="pt-7 bg-[#FAF9F5]">
  <div class="mx-auto max-w-5xl ">
  <div class="mx-auto max-w-2xl bg-[#FAF9F5] flex flex-col">
    
    <!-- Main Content -->
     <main class="max-w-2xl mx-auto w-full px-6 pb-5">
      
      <!-- Header -->
      <p class="text-amber-500 font-medium ">Event Day</p>
      <h1 class=" text-3xl font-bold text-gray-900 sm:text-4xl">Schedule</h1>
      <div class="w-33 h-[2px] bg-[#EE9F27] "></div>
      
      <!-- Description -->
      <p class="text-gray-600 mb-9 mt-7">
        The full schedule will be confirmed 2–3 weeks before the event. Join us for an evening of craft beer tasting, food pairing, brewery stories, and networking with fellow beer enthusiasts. Explore unique flavors and discover the art of Cambodian craft brewing.
      </p>

      <!-- Schedule Items -->
      <div class="flex flex-col gap-0">
        <div 
        <div 
          v-for="(item, index) in schedules" 
          :key="index"
          class="border-b border-amber-500 pb-4 mb-4"
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
    desc: 'Guest arrive , collect tasted product',
  },
  {
    time: '3 : 15 PM',
    title: 'Welcome Speech',
    desc: 'Brief presentation about the brewery, brewing process, and today',
  },
  {
    time: '3 : 30 PM',
    title: 'Door Open',
    desc: 'Guest arrive , collect tasted product',
  },
   {
    time: '6 : 40 PM',
    title: 'Door Open',
    desc: 'Guest arrive , collect tasted product',
  },
   {
    time: '7 : 30 PM',
    title: 'Door Open',
    desc: 'Guest arrive , collect tasted product',
  },
   {
    time: '8 : 30 PM',
    title: 'Door Open',
    desc: 'Guest arrive , collect tasted product',
  },
  {
    time: '8 : 30 PM',
    title: 'Door Open',
    desc: 'Guest arrive , collect tasted product',
  },
]
</script>