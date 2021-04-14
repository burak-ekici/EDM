<template>
  <div class="containeur flex justify-center flex-col">
    <div>
      <p class="text-xl md:text-3xl lg:text-4xl titre font-bold">
        <i class="fas fa-trophy"></i
        ><span class="number text-2xl md:text-3xl lg:text-4xl">1</span
        ><sup class="number text-xs md:text-2xl"> ère</sup>
        plateforme web de montage de mobilier
      </p>
    </div>
    <div class="img">
      <img src="banniere.png" alt="" />
    </div>
    <div class="phrase2 -mt-40 md:-mt-40 xl:-mt-4 2xl:mt-40">
      <p class="md:text-lg text-xs lg:text-2xl">
        <i class="fas fa-map-marked"></i>Nous intervenons sur l’ensemble de la
        France, la Suisse et tout le Bénélux francophone
      </p>
    </div>
    <div class="mx-auto mt-4">
      <v-hover v-slot="{ hover }">
        <v-btn
          :key="componentKey"
          :small="size"
          color="#2A335D"
          :elevation="hover ? 3 : 0"
          class="mt-2 white--text"
          @click="dialog = true"
          >Nous contacter</v-btn
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
            <v-btn elevation="0" color="cyan darken-2 white--text"
              >Valider</v-btn
            >
          </v-card-actions>
        </v-card>
      </v-dialog>
    </div>
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

<style scoped lang="scss">
.boutton2 {
  background-color: #3a4888;
}
.boutton2:hover {
  background-color: #2a335d;
}
.containeur {
  width: 100%;
  margin-top: 150px;
  .img {
    height: 350px;
    margin-top: 0px;
    img {
      width: 70%;
      margin: 0 auto;
      @media (max-width: 768px) {
        width: 90%;
      }
    }
  }

  div {
    .titre:after {
      content: "";
      display: block;
      background: #3a4888;
      height: 5px;
      width: 60%;
      transform: skew(-280deg);
      margin: 0 auto;
    }
    p {
      width: 60%;
      display: block;
      margin: 0px auto;
      text-align: center;
      font-family: "Raleway", sans-serif;
      font-weight: 900;

      i {
        margin-right: 15px;
        color: #ebd634;
      }
    }
  }
  .phrase2 {
    p {
      display: block;
      width: 40%;

      @media (max-width: 768px) {
        width: 50%;
      }
      @media (max-width: 640px) {
        width: 60%;
      }
      @media (min-width: 1536px) {
        margin-top: 50px;
      }
      @media (min-width: 1900px) {
        margin-top: 150px;
      }
      i {
        font-size: 2rem;
        color: #3a4888;
        @media (max-width: 768px) {
          font-size: 1rem;
        }
      }
      .france {
        color: #f1c40f;
      }
      .benelux {
        color: #f1c40f;
      }
    }
  }
}
</style>