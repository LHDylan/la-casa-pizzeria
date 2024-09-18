<template>
    <section id="menu" class="bg-[#465b4c] py-16 shadow-2xl relative">
      <div class="corner-decoration-top-right top-0 right-0"></div>
      <div class="left-decoration top-20 -left-60"></div>
      <div class="max-w-5xl container mx-auto lg:border-2 border-[#f2d0aa] rounded-lg lg:shadow-2xl py-12 px-12 lg:bg-[#2c3a30] text-white">
        <h2 class="text-3xl font-bold text-center mb-8">Nos Pizzas</h2>
        <ul class="grid gap-8">
          <li v-for="(pizza, index) in pizzas" :key="index" class="border-b border-[#f2d0aa] pb-4">
            <h3 class="text-xl font-semibold">{{ pizza.name }} <span class="float-right">{{ pizza.price }} €</span></h3>
            <p class="text-gray-300">{{ pizza.ingredients }}</p>
          </li>
        </ul>
      </div>
      <div class="right-decoration bottom-80 right-10">
        <!-- <div class="middle-"></div> -->
      </div>
      <div class="corner-decoration-bottom-left bottom-0 left-0"></div>
    </section>
  </template>
  
  <script setup>
  const pizzas = [
    { name: 'MARGARITA', price: 10, ingredients: 'Tomate, mozzarella, basilic, huile d\'olive' },
    { name: 'COCOTTE', price: 11, ingredients: 'Tomate, mozzarella, deux œufs, basilic, huile d\'olive' },
    { name: 'REGINA', price: 12, ingredients: 'Tomate, mozzarella, jambon blanc, champignons' },
    { name: '4 FROMAGES', price: 13, ingredients: 'Tomate, mozzarella, fromage de chèvre, gorgonzola, parmezan' },
    { name: 'SERRANO', price: 13, ingredients: 'Tomate, mozzarella, tomates cerises, serrano, parmezan, roquette' },
    { name: 'CALZONE', price: 13, ingredients: 'Tomate, mozzarella, jambon blanc, champignons, oeuf' },
    { name: 'CHEVRE MIEL', price: 13, ingredients: 'Crème fraîche, mozzarella, fromage de chèvre, miel' },
    { name: 'CHORIZO', price: 13, ingredients: 'Tomate, mozzarella, chorizo, poivrons' },
    { name: 'COPPA', price: 13, ingredients: 'Tomate, mozzarella, coppa, chèvre, roquette' },
    { name: 'VENTRECHE', price: 13, ingredients: 'Tomate, mozzarella, ventrêche, deux oeufs' },
    { name: 'LA CAZA', price: 14, ingredients: 'Crème fraîche, mozzarella, jambon blanc, fourme d\'Amber, champignons' },
    { name: 'POULET MOUTARDE', price: 14, ingredients: 'Crème fraîche, mozzarella, moutarde, poulet, champignons' },
    { name: 'CALZONE PLUS', price: 14, ingredients: 'Tomate, mozzarella, jambon blanc, viande hachée, champignons, oeuf' },
    { name: 'TRUITE DES PYRENEES', price: 14, ingredients: 'Crème fraîche, mozzarella, gorgonzola, truite fumée des Pyrénées, citron, roquette, huile d\'olive' },
    { name: 'CALZONE CAMEMBERT', price: 15, ingredients: 'Tomate, mozzarella, camembert, jambon blanc, huile d\'olive' },
    { name: 'TRUFFE', price: 15, ingredients: 'Tomate, mozzarella, serrano, fromage de vache à la truffe, roquette, huile d\'olive' },
    { name: 'BURRATA', price: 15, ingredients: 'Tomate, mozzarella, burrata, serrano, roquette, crème balsamique' },
  ];
  </script>