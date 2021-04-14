<template>
  <div>
    <v-hover v-slot="{ hover }">
      <v-btn
        :key="componentKey"
        color="amber"
        :small="small"
        :elevation="hover ? 3 : 0"
        class="mt-2 white--text"
        @click="dialog = true"
        >Connexion</v-btn
      ></v-hover
    >
    <v-dialog v-model="dialog" width="400px">
      <v-card light class="overlay-card">
        <h1 class="text-center text-xl font-bold my-4">
          Vous serez redirigé sur une autre page
        </h1>

        <v-card-actions>
          <v-btn
            elevation="0"
            @click="dialog = false"
            color="amber"
            class="white--text"
            >Annuler</v-btn
          >
          <v-spacer></v-spacer>
          <v-btn elevation="0" color="cyan darken-2 white--text"
            ><a
              class="white--text"
              href="http://www.artisansdesreseaux.fr/connexion"
              >Se connecter</a
            ></v-btn
          >
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dialog: false,
      fixed: true,
      small: "",
      componentKey: 0,
    };
  },
  mounted() {
    if (window.matchMedia("(max-width:1023px)").matches) {
      this.small = true;
    } else if (window.matchMedia("(min-width:1024px)").matches) {
      this.small = false;
    }

    window.addEventListener("resize", () => {
      this.small = window.matchMedia("(max-width:1023px)").matches
        ? true
        : false;
      this.forceRerender;
    });
  },
  computed: {
    size() {
      return this.small;
    },
  },
  methods: {
    forceRerender: function () {
      this.componentKey += 1;
    },
  },
};
</script>

<style>
</style>