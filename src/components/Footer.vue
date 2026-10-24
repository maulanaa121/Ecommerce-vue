<template>
  <footer class="bg-gray-950 text-gray-300 pt-12 pb-6">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-8">
        <div>
          <h3 class="text-xl font-bold text-white mb-4">Scent Haven</h3>
          <p class="mb-4">
            Your premier destination for luxury fragrances from around the world.
          </p>

          <div class="flex space-x-4">
            <a v-for="(social, index) in socialLinks" :href="social.url" :key="index" class="text-gray-400 hover:text-white transition">
                <Icon :icon="social.icon" class="w-5 h-5" />
            </a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { ref } from 'vue';

const quickLinks = ref([
  'Home',
  'Shop',
  'New Arrivals',
  'Best Sellers',
  'Gift Sets'
]);

const customerService = ref([
  'Contact Us',
  'FAQs',
  'Shipping Policy',
  'Returns & Exchanges',
  'Privacy Policy'
]);

const paymentIcons = ref([
  'logos:visa',
  'logos:mastercard',
  'logos:paypal'
]);

const socialLinks = ref([
  { icon: 'fa6-brands:facebook-f', url: '#' },
  { icon: 'fa6-brands:twitter', url: '#' },
  { icon: 'fa6-brands:instagram', url: '#' }
]);
</script>

