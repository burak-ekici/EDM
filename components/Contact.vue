<template >
  <div>
    <v-hover v-slot="{ hover }">
      <v-btn
        :key="componentKey"
        :small="size"
        color="#2A335D"
        :elevation="hover ? 3 : 0"
        class="mt-2 white--text"
        @click="dialog = true"
        >Contact</v-btn
      ></v-hover
    >
    <v-dialog v-model="dialog" width="500px">
      <v-card light class="overlay-card">
        <v-card-title>
          <h1 class="text-yellow-600">Formulaire de contact</h1>
        </v-card-title>
        <v-card-text>
          <v-form class="px-3">
            <v-text-field
              prepend-inner-icon="mdi-account"
              color="#D69E2E"
              label="Nom"
              v-model="nom"
            ></v-text-field>
            <v-text-field
              prepend-inner-icon="mdi-email"
              color="#D69E2E"
              label="Mail"
              v-model="mail"
            ></v-text-field>
            <v-textarea
              prepend-inner-icon="mdi-message-text"
              color="#D69E2E"
              label="Message"
              :clearable="clearable"
              v-model="message"
            ></v-textarea>
          </v-form>
        </v-card-text>
        <v-card-actions>
          <v-btn
            elevation="0"
            @click="dialog = false"
            color="amber"
            class="white--text"
            >Annuler</v-btn
          >
          <v-spacer></v-spacer>
          <v-btn elevation="0" color="cyan darken-2 white--text">Valider</v-btn>
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
      nom: "",
      mail: "",
      message: "",
      clearable: true,
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