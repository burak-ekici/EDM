<template>
  <div
    class="flex flex-wrap flex-col items-center lg:flex-row justify-evenly p-8"
  >
    <h1
      class="w-full text-center text-xl md:text-2xl lg:text-4xl font-bold my-20"
    >
      Nos Locaux
    </h1>
    <!-- component 1-->

    <div class="max-w-xs rounded overflow-hidden shadow-lg my-4">
      <img
        class="w-full"
        src="https://cdn.paris.fr/paris/2020/05/12/huge-67a65318e89c13e2b63ddbe2bb89cc3c.jpg"
        alt="Sunset in the mountains"
      />
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">PARIS</div>
        <p class="font-bold text-grey-darker text-base">
          2 bis Rue SQUARE CARPEAUX <br />
          75018 PARIS 18
        </p>
        <div class="mt-6 font-bold">
          <i class="fas fa-phone-alt"></i> 06 65 65 65 65
        </div>
      </div>
    </div>
    <!-- component 2-->
    <div class="max-w-xs rounded overflow-hidden shadow-lg my-4">
      <img
        class="w-full"
        src="https://www.myexpat.fr/wp-content/uploads/panorama-immobilier-lyon.jpeg"
        alt="Sunset in the mountains"
      />
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">LYON</div>
        <p class="font-bold text-grey-darker text-base">
          2 bis Rue SQUARE CARPEAUX <br />
          75018 PARIS 18
        </p>
        <div class="mt-6 font-bold">
          <i class="fas fa-phone-alt"></i> 06 65 65 65 65
        </div>
      </div>
    </div>
    <!-- component 3-->
    <div class="max-w-xs rounded overflow-hidden shadow-lg my-4">
      <img
        class="w-full"
        src="https://blog.laou.fr/wp-content/uploads/2020/02/vivre_a_orleans-1200x675.jpg"
        alt="Sunset in the mountains"
      />
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">ORLEANS</div>
        <p class="font-bold text-grey-darker text-base">
          2 bis Rue SQUARE CARPEAUX <br />
          75018 PARIS 18
        </p>
        <div class="mt-6 font-bold">
          <i class="fas fa-phone-alt"></i> 06 65 65 65 65
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.rounded:hover {
  transform: scale(1.05);
  box-shadow: 0 5px 5px rgba(0, 0, 0, 0.3);
}
.rounded {
  transition: all 0.2s;
}
img {
  height: 200px;
}
</style>