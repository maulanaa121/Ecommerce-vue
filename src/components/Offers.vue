<template>
    <div id="offers" class="container scroll-mt-20 mx-auto px-4 py-12" >
        <h2 class="text-3xl font-bold text-center mb-2 text-amber-900" >
            Special Offers
        </h2>
        <p class="text-center text-gray-600 mb-12">Take advantage of these limited-time offers</p>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">            
            <div v-for="offer in currentOffers" :key="offer.id" :class="[ offer.bgColor,'rounded-xl shadow-lg overflow-hidden transition-transform duration-300 hover:scale-105']" >
                <div class="p-6">
                    <div class="flex justify-between items-start mb-4">
                        <h3 :class="[offer.textColor, 'text-xl font-semibold']">
                            {{ offer.title }}
                        </h3>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>

import { ref } from 'vue';
    const currentOffers = ref([
        [
  {
    id: 1,
    title: 'Hot Summer Sale',
    description: 'Up to 30% off on our summer perfume collection',
    discount: '30%',
    endDate: '2023-08-31',
    code: 'SUMMER30',
    bgColor: 'bg-amber-200',
    textColor: 'text-amber-700'
  },
  {
    id: 2,
    title: 'Autumn Special',
    description: 'Get 20% off on all warm and woody scents',
    discount: '20%',
    endDate: '2023-10-31',
    code: 'AUTUMN20',
    bgColor: 'bg-orange-200',
    textColor: 'text-orange-800'
  },
  {
    id: 3,
    title: 'Winter Flash Sale',
    description: 'Flat 50% discount on luxury gift sets',
    discount: '50%',
    endDate: '2023-12-25',
    code: 'WINTER50',
    bgColor: 'bg-blue-200',
    textColor: 'text-blue-800'
  }
]
    ])

</script>