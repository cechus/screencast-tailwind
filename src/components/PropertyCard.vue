<template>
  <div class="max-w-sm mr-10 mb-10">
    <!-- <div class="h-48 bg-cover bg-center" :style="{ backgroundImage: `url('${property.imageUrl}')`}"></div> -->
    <div class="relative pb-5/6 ">
        <img class="absolute h-full  w-full object-cover rounded-lg shadow-md" :src="property.imageUrl" alt />
    </div>
    <div class="relative z-10 px-4 -mt-16">
        <div class="bg-white p-6 rounded-lg shadow-lg">
            <div class="flex items-baseline">
                <span class="inline-block bg-red-200 text-red-500 font-semibold text-white text-xs px-2 rounded-full uppercase tracking-wider mr-2">New</span>
                <div class="text-gray-600 text-xs uppercase font-semibold tracking-wide">
                    {{property.beds}} beds &bull; {{ property.baths }} baths
                </div>
            </div>
            <h4 class="font-semibold text-lg leading-tight truncate">{{ property.title }}</h4>
            <div class="mt-1">{{ property.formattedPrice }}
                <span class="text-gray-600 text-sm"> / wk</span>
            </div>
            <div class="mt-2 flex items-center">
                <svg v-for="i in 5" :key="i" :class="i <= property.rating ? 'text-red-500' : 'text-gray-500'" class="h-5 w-5 fill-current" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                    <path d="M6.1 21.98a1 1 0 0 1-1.45-1.06l1.03-6.03-4.38-4.26a1 1 0 0 1 .56-1.71l6.05-.88 2.7-5.48a1 1 0 0 1 1.8 0l2.7 5.48 6.06.88a1 1 0 0 1 .55 1.7l-4.38 4.27 1.04 6.03a1 1 0 0 1-1.46 1.06l-5.4-2.85-5.42 2.85zm4.95-4.87a1 1 0 0 1 .93 0l4.08 2.15-.78-4.55a1 1 0 0 1 .29-.88l3.3-3.22-4.56-.67a1 1 0 0 1-.76-.54l-2.04-4.14L9.47 9.4a1 1 0 0 1-.75.54l-4.57.67 3.3 3.22a1 1 0 0 1 .3.88l-.79 4.55 4.09-2.15z"/>
                </svg>
                <!-- <span class="text-red-600 font-semibold">
                {{ property.rating }}/5 starts
                </span> -->
                <span class="ml-2 text-gray-600 text-sm">
                {{ property.reviewCount }} reviews
                </span>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['property']
}
</script>
