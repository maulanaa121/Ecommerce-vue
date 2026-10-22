<template>
    <section id="categories">
        <div class="container mx-auto px-4">
        <!-- Section Header -->
        <div class="text-center mb-12">
            <h2 class="text-3xl font-bold text-amber-950 mb-3">
                Explore Our Fragrance Collections
            </h2>

            <p class="text-lg text-gray-800 max-w-2xl mx-auto">
                Discover scents that match your personality
            </p>
        </div>

        <!-- Categories Grid -->
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
            <div v-for="(category, index) in categories" :key="index" class="relative group overflow-hidden rounded-lg shadow-md hover:shadow-lg trasnition-shadow duration-300">
                <div class="h-64 overflow-hidden">
                    <img :src="category.image" :alt="category.alt" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                </div>
                <div class="absolute inset-0 bg-gradient-to-t from-black/60 via-transparent to-transparent">
                    <div class="absolute bottom-0 left-0 p-6">
                        <h3 class="">{{ category.title }}</h3>
                        <p class="text-gray-200">{{ category.description }}</p>
                    </div>
                </div>
            </div>
        </div>
        </div>
    </section>
</template>
<script setup>
import { ref } from 'vue';

const productImages = import.meta.glob('../assets/product*.png', {
    eager: true,
    import: 'default'
});

const categories = ref([
    {   
        title:"Men's collection",
        image:productImages['../assets/product8.png'],
        description : "Bold & masculine scents",
        alt:"Men's collection"
    },
    {   
        title: "Women's collection",
        image: productImages['../assets/product9.png'],
        description: "Elegant & floral fragrances",
        alt: "Women's collection"
    },
    {   
        title: "Unisex collection",
        image: productImages['../assets/product10.png'],
        description: "Versatile & balanced blends",
        alt: "Unisex collection"
    },
    {   
        title: "Summer fresh",
        image: productImages['../assets/produc11.png'],
        description: "Light, citrus & refreshing notes",
        alt: "Summer fresh collection"
    },
    {   
        title: "Luxury oud & spice",
        image: productImages['../assets/product12.png'],
        description: "Rich, warm & exotic oriental scents",
        alt: "Luxury oud & spice collection"
    },
    {   
        title: "Limited edition",
        image: productImages['../assets/product13.png'],
        description: "Exclusive & rare aromatic craft",
        alt: "Limited edition collection"
    }
])
</script>