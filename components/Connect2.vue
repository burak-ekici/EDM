<template >
  <div>
    <v-hover v-slot="{ hover }">
      <v-btn
        color="amber"
        :elevation="hover ? 3 : 0"
        class="mt-2 white--text"
        @click="dialog = true"
        >Connexion</v-btn
      ></v-hover
    >
    <v-dialog v-model="dialog" width="500px">
      <v-card light class="overlay-card">
        <v-card-title>
          <h1 class="text-yellow-600">Connexion</h1>
        </v-card-title>
        <v-card-text>
          <v-form class="px-3">
            <v-text-field
              prepend-inner-icon="mdi-account"
              color="#D69E2E"
              label="Compte"
              v-model="compte"
            ></v-text-field>
            <v-text-field
              :type="showpassword ? 'text' : 'password'"
              prepend-inner-icon="mdi-lock"
              :append-icon="showpassword ? 'mdi-eye' : 'mdi-eye-off'"
              color="#D69E2E"
              label="Mot de pass"
              v-model="password"
              @click:append="showpassword = !showpassword"
            ></v-text-field>
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
          <v-btn elevation="0" color="cyan darken-2 white--text"
            >Se connecter</v-btn
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
      compte: "",
      password: "",
      clearable: true,
      dialog: false,
      fixed: true,
      showpassword: false,
    };
  },
};
</script>

<style>
</style>