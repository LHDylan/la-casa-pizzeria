<template>
  <section id="gallery" class="bg-white py-16">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-bold text-center mb-8">Galerie</h2>

      <!-- Swiper Carousel -->
      <swiper-container :slides-per-view="3" :space-between="spaceBetween" :centered-slides="true" :loop="true"
        :autoplay="{ delay: 2500, disableOnInteraction: false }" :breakpoints="{
          768: {
            slidesPerView: 3,
          },
          640: {
            slidesPerView: 1,
          }
        }" @swiperprogress="onProgress" @swiperslidechange="onSlideChange" class="swiper-gallery">
        <swiper-slide v-for="(image, index) in images" :key="index" class="relative">
          <img :src="image.src" :alt="image.alt" class="object-cover w-full h-64 cursor-pointer"
            @click="openImage(image.src)" />
        </swiper-slide>
      </swiper-container>

    </div>

    <!-- Modal for displaying the enlarged image -->
    <div v-if="isModalOpen" class="fixed inset-0 z-50 flex items-center justify-center bg-black bg-opacity-75">
      <div class="relative">
        <img :src="modalImage" alt="Pizza in large view" class="max-w-full max-h-screen object-cover" />
        <button @click="closeModal" class="absolute top-2 right-2 text-white text-2xl">X</button>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

// Register Swiper elements
import { register } from 'swiper/element/bundle';
register();

// Define the images for the gallery
const images = ref([
  { src: '/img/pizza_gallery_1.jpg', alt: 'Pizza 1' },
  { src: '/img/pizza_gallery_2.jpg', alt: 'Pizza 2' },
  { src: '/img/pizza_gallery_3.jpg', alt: 'Pizza 3' },
  { src: '/img/pizza_gallery_4.jpg', alt: 'Pizza 4' },
]);

// Space between slides
const spaceBetween = 10;

// Modal state
const isModalOpen = ref(false);
const modalImage = ref('');

// Open modal with larger image
const openImage = (imageSrc) => {
  modalImage.value = imageSrc;
  isModalOpen.value = true;
};

// Close modal
const closeModal = () => {
  isModalOpen.value = false;
};

// Swiper progress event
const onProgress = (e) => {
  const [swiper, progress] = e.detail;
  console.log(progress);
};

// Swiper slide change event
const onSlideChange = (e) => {
  console.log('slide changed');
};
</script>

<style scoped>
.swiper-gallery {
  width: 100%;
  height: 300px;
}

.swiper-slide img {
  border-radius: 12px;
  transition: transform 0.3s ease;
}

.swiper-slide img:hover {
  transform: scale(1.05);
}

.swiper-button-next,
.swiper-button-prev {
  color: #465b4c;
  /* Primary color */
}

.swiper-pagination-bullet {
  background-color: #465b4c;
}

.modal img {
  max-width: 90vw;
  max-height: 90vh;
  object-fit: contain;
}
</style>
