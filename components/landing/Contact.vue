<template>
  <section id="contact" class="bg-white py-16">
    <div class="container mx-auto text-center sm:text-left px-6 grid grid-cols-1 md:grid-cols-3 gap-8">

      <!-- Informations -->
      <div class="border-b md:border-b-0 md:border-r border-gray-300 pb-4">
        <h2 class="text-3xl font-bold mb-4">Informations</h2>
        <div>
          <h2 class="text-lg font-bold">Téléphone</h2>
          <a href="tel:+33123456789" class="text-[#465b4c]">+33 1 23 45 67 89</a>
          <h2 class="text-lg font-bold mt-4">Email</h2>
          <a href="mailto:example@example.com" class="text-[#465b4c]">example@example.com</a>
          <h2 class="text-lg font-bold mt-4">Adresse</h2>
          <p>181 Rue des Pyrénées</p>
          <p>64420</p>
          <p class="uppercase">Eslourenties-Daban</p>
          <a href="https://maps.google.com/?q=181+Rue+des+Pyr%C3%A9n%C3%A9es,+64420+Eslourenties-Daban" target="_blank"
            class="inline-block bg-[#465b4c] text-white rounded-md px-4 py-2 mt-2">Google Maps</a>
          <a href="https://waze.com/ul?ll=43.298619,-0.218303&navigate=yes" target="_blank"
            class="inline-block bg-[#465b4c] text-white rounded-md px-4 py-2 mt-2 ml-4">Waze</a>
        </div>
      </div>

      <!-- Horaires -->
      <div class="border-b md:border-b-0 md:border-r border-gray-300">
        <h2 class="text-3xl font-bold mb-4">Horaires</h2>
        <ul class="mb-4">
          <li>Jeudi: Fermé</li>
          <li>Vendredi: 18:30–21:00</li>
          <li>Samedi: 18:30–21:00</li>
          <li>Dimanche: Fermé</li>
          <li>Lundi: Fermé</li>
          <li>Mardi: Fermé</li>
          <li>Mercredi: 18:30–21:00</li>
        </ul>
      </div>

      <!-- Formulaire de contact -->
      <div>
        <h2 class="text-3xl font-bold mb-4">Contactez-nous</h2>
        <form>
          <input type="text" placeholder="Nom" class="w-full mb-4 p-2 border border-gray-300 rounded-md" />
          <input type="email" placeholder="Email" class="w-full mb-4 p-2 border border-gray-300 rounded-md" />
          <textarea placeholder="Message" class="w-full mb-4 p-2 border border-gray-300 rounded-md"></textarea>
          <button type="submit" class="w-full bg-[#465b4c] text-white p-2 rounded-md">Envoyer</button>
        </form>
      </div>
    </div>
  </section>
</template>
