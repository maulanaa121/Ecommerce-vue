<template>
    <div id="offers" class="container scroll-mt-20 mx-auto px-4 py-12" >
        <h2 class="text-3xl font-bold text-center mb-2 text-amber-900" >
            Special Offers
        </h2>
        <p class="text-center text-gray-600 mb-12">Take advantage of these limited-time offers</p>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <div v-for="offer in currentOffers" :key="offer.id" >
            </div>
        </div>
    </div>
</template>
<script>
</script>