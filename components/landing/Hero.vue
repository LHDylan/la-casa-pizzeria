<!-- <template>
  <section class="relative bg-white">
    <header class="fixed inset-x-0 top-0 z-50 bg-white bg-opacity-50 backdrop-blur-md shadow-lg">
      <nav class="flex items-center justify-center p-6 lg:px-8" aria-label="Global">
        <div class="hidden lg:flex lg:gap-x-12">
          <nuxt-link href="#about" class="text-sm font-semibold leading-6 text-gray-900">À propos</nuxt-link>
          <nuxt-link href="#menu" class="text-sm font-semibold leading-6 text-gray-900">Menu</nuxt-link>
          <nuxt-link href="#gallery" class="text-sm font-semibold leading-6 text-gray-900">Galerie</nuxt-link>
          <nuxt-link href="#testimonials" class="text-sm font-semibold leading-6 text-gray-900">Témoignages</nuxt-link>
          <nuxt-link href="#contact" class="text-sm font-semibold leading-6 text-gray-900">Contact</nuxt-link>
        </div>
      </nav>
    </header>
    <div class="text-center py-32 sm:py-48 lg:py-56">
      <h1 class="text-4xl font-bold text-gray-900 sm:text-6xl">La Caza Pizzeria</h1>
      <a href="#menu" class="mt-10 inline-block bg-[#8d4537] px-5 py-3 text-sm font-semibold text-white rounded-md shadow-sm hover:bg-indigo-500">
        Voir le menu
      </a>
    </div>
  </section>
</template> -->

<template>
  <section class="relative bg-white">
    <!-- Navbar classique visible en scroll avec fond semi-opaque -->
    <header class="fixed inset-x-0 top-0 z-50 bg-white bg-opacity-80 backdrop-blur-sm shadow-lg">
      <nav class="flex items-center justify-center p-6 lg:px-8" aria-label="Global">
        <div class="hidden sm:flex sm:gap-x-12">
          <nuxt-link href="#about" class="text-sm font-semibold leading-6 text-gray-900">À propos</nuxt-link>
          <nuxt-link href="#menu" class="text-sm font-semibold leading-6 text-gray-900">Menu</nuxt-link>
          <nuxt-link href="#gallery" class="text-sm font-semibold leading-6 text-gray-900">Galerie</nuxt-link>
          <nuxt-link href="#testimonials" class="text-sm font-semibold leading-6 text-gray-900">Témoignages</nuxt-link>
          <nuxt-link href="#contact" class="text-sm font-semibold leading-6 text-gray-900">Contact</nuxt-link>
        </div>
        <!-- Menu burger pour mobile -->
        <div class="sm:hidden fixed top-4 right-4 z-50">
          <button id="burger-menu" class="text-gray-900">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
            </svg>
          </button>

          <div id="mobile-menu" class="hidden fixed top-0 right-0 h-screen w-screen bg-white bg-opacity-95 flex items-center justify-center space-x-6">
            <a href="tel:+33123456789" class="bg-[#465b4c] p-4 rounded-full text-white">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 24 24" fill="currentColor">
                <path d="M3 2h4c.6 0 1 .4 1 1v3c0 .6-.4 1-1 1H4.2c.4.6.7 1.2 1 1.9l2.2 2.2c.4.4.5 1.1.2 1.6L5.7 14c-.3.6-.1 1.3.4 1.8 1.2 1.2 2.9 2 4.6 2.1 1.1 0 2.2-.2 3.1-.6l1.1-.6c.5-.3 1.1-.2 1.6.2l2.2 2.2c.6.6 1.3.9 2 .9h3c.6 0 1-.4 1-1V21c0-.6-.4-1-1-1h-3.6c-4.1-.1-8-3.3-8.8-7.3l-.6-1.1C2.8 11.1 2 10.4 2 9.8V6.2c0-.6.4-1 1-1h3z" />
              </svg>
            </a>

            <a href="https://waze.com/ul?ll=43.298619,-0.218303&navigate=yes" target="_blank" class="bg-[#465b4c] p-4 rounded-full text-white">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19.3 12.2c1.7 0 3 1.3 3 3s-1.3 3-3 3-3-1.3-3-3 1.3-3 3-3z" />
              </svg>
            </a>

            <a href="https://maps.google.com/?q=181+Rue+des+Pyr%C3%A9n%C3%A9es,+64420+Eslourenties-Daban" target="_blank" class="bg-[#465b4c] p-4 rounded-full text-white">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 11c1.7 0 3 1.3 3 3s-1.3 3-3 3-3-1.3-3-3 1.3-3 3-3z" />
              </svg>
            </a>
          </div>
        </div>
      </nav>
    </header>

    <!-- Hero section -->
    <div class="text-center py-32 sm:py-48 lg:py-56">
      <h1 class="text-4xl font-bold text-gray-900 sm:text-6xl">La Caza Pizzeria</h1>
      <nuxt-link href="#menu" class="mt-10 inline-block bg-[#8d4537] px-5 py-3 text-sm font-semibold text-white rounded-md shadow-sm hover:bg-indigo-500">Voir le menu</nuxt-link>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  const burgerMenu = document.getElementById('burger-menu')
  const mobileMenu = document.getElementById('mobile-menu')

  burgerMenu.addEventListener('click', () => {
    mobileMenu.classList.toggle('hidden')
  })

  window.addEventListener('scroll', () => {
    if (!mobileMenu.classList.contains('hidden')) {
      mobileMenu.classList.add('hidden')
    }
  })
})
</script>