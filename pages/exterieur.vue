<template>
  <div class="interieur">
    <!-- Slider principal  -->
    <div>
      <v-app class="slider">
        <v-container>
          <h1 class="mb-4 block text-4xl font-bold text-gray-700">
            Aménagement extérieur et jardin
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
                  <span class="font-bold">Client</span> : Professionnels et
                  particuliers, municipalités… <br /><span class="font-bold"
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
                  <span class="font-bold">Abris et serres de jardin</span> :
                  abris en bois, en résine, en tôle, car park, serres en verre,
                  en plexi <br /><span class="font-bold"
                    >Gros mobilier de jardin</span
                  >
                  : cuisine extérieure, barbecue en kit, balançoires et
                  portiques <br /><span class="font-bold"
                    >Petit mobilier de jardin</span
                  >
                  : transat, chaises, tables, parasol
                  <br /><span class="font-bold"
                    >Tonnelle ou pergola autoportante</span
                  >
                  <br /><span class="font-bold"
                    >Marquise, tonnelle ou pergola semi portante </span
                  >( à fixer sur un mur ) <br />
                  <span class="font-bold"> Piscine tubulaire </span><br />
                  <span class="font-bold"> Gros mobilier urbain</span> : aire de
                  jeu pour enfant, gradins… <br />
                  <span class="font-bold">
                    Petit mobilier urbain à fixer au sol</span
                  >
                  : poubelle, banc, table de pique nique, panneau de direction
                  en bois <br /> </v-card-text></v-card
            ></v-col>
            <v-col cols="12" xs="12" sm="12" md="4" class=""
              ><v-card color="#f1f1f1" class="card">
                <v-card-title
                  class="text-center font-bold text-2xl text-yellow-500"
                >
                  Les Projets
                </v-card-title>
                <v-card-text class="">
                  <span class="font-bold"
                    >Un service d’installation sur toute la France et la
                    Belgique pour vos produits, directement chez vos clients
                    particuliers ou collectivités. <br /><br />
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
          src="https://www.youtube.com/embed/3-SnuYwE7xg"
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
          src: "/exterieur/slider1/1.png",

          alt: "Mobilier pour collectivités",
        },

        {
          src: "/exterieur/slider1/2.png",

          alt: "Abri de jardin",
        },
        {
          src: "/exterieur/slider1/3.png",

          alt: "Mobilier universitaire",
        },
        {
          src: "/exterieur/slider1/4.png",

          alt: "Racks et rayonnages",
        },
      ],
      slider2: [
        {
          src: "/exterieur/1.png",

          alt: "Mobilier pour collectivités",
        },

        {
          src: "/exterieur/2.png",

          alt: "Abri de jardin",
        },
        {
          src: "/exterieur/3.png",

          alt: "Mobilier universitaire",
        },
        {
          src: "/exterieur/4.png",

          alt: "Racks et rayonnages",
        },
        {
          src: "/exterieur/5.png",

          alt: "Racks et rayonnages",
        },
      ],
    };
  },
};
</script>

<style>
</style>