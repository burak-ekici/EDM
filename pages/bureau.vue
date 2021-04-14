<template>
  <div class="interieur">
    <!-- Slider principal  -->
    <div>
      <v-app class="slider">
        <v-container>
          <h1 class="mb-4 block text-4xl font-bold text-gray-700">
            Pose de mobilier de bureau
          </h1>
          <v-main class="h-full">
            <v-carousel
              cycle
              hide-delimiters
              height="650px"
              class="elevation-20"
            >
              <v-carousel-item
                class="h-full"
                v-for="(item, i) in items"
                :key="i"
                :src="item.src"
                :alt="item.alt"
              >
              </v-carousel-item>
            </v-carousel> </v-main
        ></v-container>
      </v-app>
    </div>
    <!-- Section card -->
    <div>
      <div>
        <v-container elevation="0" class="my-20">
          <v-row justify="center">
            <v-col cols="12" xs="12" sm="12" md="4"
              ><v-card color="#f1f1f1" class="card">
                <v-card-title
                  class="text-center font-bold text-2xl text-yellow-500"
                >
                  DESCRIPTION
                </v-card-title>
                <v-card-text class="text-red-300">
                  <span class="font-bold">Client</span> : siège sociaux,
                  coworking, bureaux en open space <br /><span class="font-bold"
                    >Localisation</span
                  >
                  : France, Belgique, Suisse, Luxembourg
                  <br />
                  <br /><br /><br /><br /> </v-card-text></v-card
            ></v-col>
            <v-col cols="12" xs="12" sm="12" md="4" class=""
              ><v-card color="#f1f1f1" class="card">
                <v-card-title class="font-bold text-2xl text-yellow-500">
                  Exemples
                </v-card-title>
                <v-card-text class="text-white">
                  <span class="font-bold"
                    >Cabines et cloisons modulaires de bureau</span
                  >
                  : cabines de sieste, cabines insonorisée, cloisons
                  modulaires<br /><span class="font-bold"
                    >Gros mobilier de bureau</span
                  >
                  : grands bureaux partagés, étagères en kit en tôle ou
                  aggloméré, dressings, casiers, racks <br /><span
                    class="font-bold"
                    >Petit mobilier de bureau</span
                  >
                  : chaises, petit élément de rangement, décoration murale
                </v-card-text></v-card
              ></v-col
            >
            <v-col cols="12" xs="12" sm="12" md="4" class=""
              ><v-card color="#f1f1f1" class="card">
                <v-card-title
                  class="text-center font-bold text-2xl text-yellow-500"
                >
                  Les Projets
                </v-card-title>
                <v-card-text class="">
                  <span class="font-bold"
                    >Des équipes professionnelles disponibles pour
                    l’installation et le montage du mobilier de vos plateaux de
                    bureau. <br /><br />
                    <br />
                    <br />
                    <br
                  /></span> </v-card-text></v-card
            ></v-col>
          </v-row>
        </v-container>
      </div>
    </div>
    <!-- slider secondaire  -->
    <div>
      <v-app class="slider2" height="550px">
        <v-container>
          <v-main class="h-full">
            <v-carousel
              cycle
              hide-delimiters
              height="550px"
              class="elevation-20"
            >
              <v-carousel-item
                class="h-full"
                v-for="(image, i) in slider2"
                :key="i"
                :src="image.src"
                :alt="image.alt"
              >
              </v-carousel-item>
            </v-carousel> </v-main
        ></v-container>
      </v-app>
    </div>
    <!-- Video  -->
    <div class="mb-10">
      <v-container>
        <iframe
          width="100%"
          height="600"
          src="https://www.youtube.com/embed/MoZRsyJEh4Q"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          src: "/bureau/slider1/1.png",

          alt: "Mobilier pour collectivités",
        },

        {
          src: "/bureau/slider1/2.png",

          alt: "Abri de jardin",
        },
        {
          src: "/bureau/slider1/3.png",

          alt: "Mobilier universitaire",
        },
      ],
      slider2: [
        {
          src: "/bureau/1.jpg",

          alt: "Mobilier pour collectivités",
        },

        {
          src: "/bureau/2.png",

          alt: "Abri de jardin",
        },
        {
          src: "/bureau/3.png",

          alt: "Mobilier universitaire",
        },
        {
          src: "/bureau/4.png",

          alt: "Racks et rayonnages",
        },
        {
          src: "/bureau/5.jpg",

          alt: "Racks et rayonnages",
        },
      ],
    };
  },
};
</script>

<style>
</style>