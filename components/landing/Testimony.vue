<template>
  <section id="testimonials" class="bg-[#8d4537] py-16 z-0 shadow-2xl relative">
    <div class="top-decoration top-0 -left-40"></div>
    <div class="container mx-auto px-6 text-white">
      <h2 class="text-3xl font-bold text-center mb-8">Témoignages</h2>
      <ul class="grid gap-8 lg:grid-cols-3">

        <li v-for="(testimonial, index) in testimonials" :key="index" class="bg-white text-[#8d4537] p-4 rounded-lg shadow-2xl">
          <div class="flex justify-between items-center">
            <h3 class="text-lg font-semibold">{{ testimonial.author }}</h3>
            <span>{{ testimonial.date }}</span>
          </div>
          <p class="mt-2">{{ testimonial.text }}</p>
          <div class="mt-4">
            <span v-for="n in 5" :key="n" class="inline-block">
              <svg v-if="n <= testimonial.rating" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 24 24" stroke="currentColor" class="w-5 h-5 text-yellow-500">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 2l2.09 6.26H21l-5.34 3.88L16.18 18 12 13.92 7.82 18l1.43-5.86L3.91 8.26H9.9z"/>
              </svg>
              <svg v-else xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="w-5 h-5">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 2l2.09 6.26H21l-5.34 3.88L16.18 18 12 13.92 7.82 18l1.43-5.86L3.91 8.26H9.9z"/>
              </svg>
            </span>
          </div>
        </li>

      </ul>
    </div>
    <div class="bottom-decoration bottom-0 right-10"></div>
  </section>
</template>

<script setup>
const testimonials = [
  { author: 'Jean Dupont', date: '10/09/2024', text: 'Excellente pizza, service rapide et chaleureux.', rating: 5 },
  { author: 'Marie Lemoine', date: '05/09/2024', text: 'La meilleure pizzeria du coin, je recommande !', rating: 4 },
  { author: 'Luc Martin', date: '03/09/2024', text: 'Des pizzas délicieuses mais un peu trop d’attente.', rating: 3 },
];
</script>
