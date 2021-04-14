<template>
  <div class="mt-40 lg:mt-64 relative mb-48">
    <v-app class="slider">
      <v-container>
        <h1 class="mb-4 block text-xl md:text-2xl lg:text-4xl font-bold">
          Prestations
        </h1>
        <v-main class="h-full">
          <v-carousel cycle hide-delimiters height="650px" class="elevation-20">
            <v-carousel-item
              class="h-full"
              v-for="(item, i) in items"
              :key="i"
              :src="item.src"
              :alt="item.alt"
            >
              <v-sheet
                class="grey--text grey lighten-2 pl-4 py-3 font-bold text-xl"
              >
                {{ item.title }}
              </v-sheet>
            </v-carousel-item>
          </v-carousel>
        </v-main></v-container
      >
    </v-app>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          src: "collectivite.jpeg",
          title: "Mobilier pour collectivités",
          alt: "Mobilier pour collectivités",
        },

        {
          src: "abri.jpeg",
          title: "Abri de jardin",
          alt: "Abri de jardin",
        },
        {
          src: "ecole.jpeg",
          title: "Mobilier universitaire",
          alt: "Mobilier universitaire",
        },
        {
          src: "racks.jpeg",
          title: "Racks et rayonnages",
          alt: "Racks et rayonnages",
        },
        {
          src: "hopital.jpeg",
          title: "Mobilier pour collectivités",
          alt: "Mobilier pour collectivités",
        },
        {
          src: "salon.jpeg",
          title: "Aménagement de mobilier d'intérieur",
          alt: "Aménagement de mobilier d'intérieur",
        },
        {
          src: "jeux.jpeg",
          title: "Aménagement extérieur",
          alt: "Aménagement extérieur",
        },
      ],
    };
  },
};
</script>

<style scoped>
h1 {
  margin-top: -100px;

  font-family: "Raleway", sans-serif;
}
</style>