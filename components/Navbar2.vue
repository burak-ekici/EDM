<template>
  <div class="">
    <div class="flex justify-between items-center containeur fixed">
      <div class="w-full text-gray-700 bg-white">
        <div
          class="flex flex-row items-center px-4 md:items-center md:justify-between md:flex-row md:px-6 lg:px-8"
        >
          <div class="p-4 flex flex-row items-center justify-between">
            <nuxt-link to="/"
              ><img src="logo.png" alt="logo EDM" width="120px"
            /></nuxt-link>
          </div>
          <!-- button 3 barre -->
          <div class="flex justify-end items-center md:hidden mobile">
            <button
              type="button"
              class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
              aria-expanded="false"
              @click="mobilelist = !mobilelist"
            >
              <svg
                class="h-6 w-6"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                aria-hidden="true"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6h16M4 12h16M4 18h16"
                />
              </svg>
            </button>
            <transition name="list-mobile">
              <div
                class="mobile-list"
                v-if="mobilelist === true"
                v-click-outside="mobilelistOff"
              >
                <button
                  type="button"
                  class="mt-4 cross bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
                  aria-expanded="false"
                  @click="mobilelist = !mobilelist"
                >
                  <v-icon large>mdi-close</v-icon>
                </button>
                <ul class="pl-0 space-y-8 font-bold mt-8">
                  <li @click="mobilelist = !mobilelist">
                    <nuxt-link to="/">Accueil</nuxt-link>
                  </li>
                  <li @click="mobilelist = !mobilelist">
                    <nuxt-link to="/services">Nos services</nuxt-link>
                  </li>
                  <li @click="mobilelist = !mobilelist">
                    <nuxt-link to="/nous">Qui somme nous ?</nuxt-link>
                  </li>
                  <li>
                    <Contact class="button-scale" />
                  </li>
                  <li>
                    <Connect class="button-scale" />
                  </li>
                </ul>
              </div>
            </transition>
          </div>

          <!-- button 3 barre  -->
          <nav
            class="flex-col flex-grow flex items-center md:pb-0 hidden md:flex md:justify-end md:flex-row"
          >
            <nuxt-link
              class="px-4 py-2 mt-2 text-xs lg:text-sm font-semibold bg-transparent rounded-lg md:mt-0 hover:text-gray-900 focus:text-gray-900 hover:bg-gray-200 focus:bg-gray-200 focus:outline-none"
              to="/"
              >Acceuil</nuxt-link
            >
            <nuxt-link
              class="services px-4 py-2 mt-2 text-xs lg:text-sm font-semibold bg-transparent rounded-lg md:mt-0 hover:text-gray-900 focus:text-gray-900 hover:bg-gray-200 focus:bg-gray-200 focus:outline-none"
              to="/services"
              >Nos services de montage</nuxt-link
            >
            <nuxt-link
              class="px-4 py-2 mt-2 text-xs lg:text-sm font-semibold bg-transparent rounded-lg md:mt-0 md:ml-4 hover:text-gray-900 focus:text-gray-900 hover:bg-gray-200 focus:bg-gray-200 focus:outline-none"
              to="/nous"
              >Qui sommes nous ?</nuxt-link
            >

            <Contact class="ml-6" />
            <div class="relative">
              <Connect class="ml-6" />
            </div>
          </nav>
        </div>
      </div>
    </div>
    <!-- Hover effect  -->
    <transition name="list">
      <div v-show="open" class="hover-el rounded-md mt-6 text-center text-md">
        <ul>
          <li class="flex">
            <nuxt-link to="/interieur">
              <img src="/interieur.svg" alt="" /> Aménagement<br />
              intérieur</nuxt-link
            >
          </li>
          <li>
            <nuxt-link to="/exterieur">
              <img src="/jardin.svg" alt="" />Aménagement<br />
              extérieur et jardin</nuxt-link
            >
          </li>
          <li>
            <nuxt-link to="/bureau">
              <img src="/bureau.svg" alt="" />Pose de<br />
              mobilier de bureau</nuxt-link
            >
          </li>
          <li>
            <nuxt-link to="/retail">
              <img src="/retail.svg" alt="" />Pose de<br />
              mobilier Retail</nuxt-link
            >
          </li>
          <li>
            <nuxt-link to="/rayonnage">
              <img src="/rayonnage.svg" alt="" />Installation<br />
              de racks et rayonnages</nuxt-link
            >
          </li>
          <li>
            <nuxt-link to="/specialise">
              <img src="/collectivite.svg" alt="" />Pose de<br />
              mobilier spécialisé</nuxt-link
            >
          </li>
        </ul>
      </div>
    </transition>

    <!-- Hover effect  -->
  </div>
</template>

<script>
import Contact from "./Contact";
export default {
  components: { Contact },
  mounted() {
    window.addEventListener("DOMContentLoaded", () => {
      const conteneur = document.querySelector(".containeur");
      window.addEventListener("scroll", () => {
        if (window.scrollY > 0) {
          conteneur.style.boxShadow = "0 5px 5px rgba(0,0,0,0.5)";
        } else {
          conteneur.style.boxShadow = "";
        }
      });
    });
    const hoverlink = document.querySelector(".services");
    const liste = document.querySelector(".hover-el");
    const li = document.querySelectorAll(".hover-el ul li");
    let MouseInList = false;
    let MouseInLink = false;
    hoverlink.addEventListener("mouseenter", () => {
      this.open = true;
      MouseInLink == true;
      liste.addEventListener("mouseenter", () => {
        MouseInList = true;
        MouseInLink = false;
        liste.addEventListener("mouseleave", () => {
          this.open = false;
          MouseInLink = false;
          MouseInList = false;
        });
      });
      hoverlink.addEventListener("mouseleave", () => {
        setTimeout(() => {
          if (MouseInList === false) {
            this.open = false;
          }
        }, 200);
      });
    });
    li.forEach((el) => {
      el.addEventListener("click", () => {
        this.open = false;
      });
    });
  },
  data() {
    return {
      open: false,
      overlay: false,
      mobilelist: false,
    };
  },
  transition: { name: "home" },
  methods: {
    mobilelistOff() {
      if (this.mobilelist === true) {
        this.mobilelist = false;
      }
    },
  },
};
</script>

<style scoped lang="scss">
.containeur {
  font-family: "Roboto", sans-serif;
  box-sizing: border-box;
  width: 100%;
  height: auto;
  transition: All 0.7s;
  text-align: center;

  &.fixed {
    position: fixed;
    background: white;
    top: 0;
    left: 0;
    right: 0;
    transition: All 0.7s;
    z-index: 50;
    height: 8%;
  }
  .img {
    width: 15%;
    img {
      width: 150px;
      margin: 25px 50px;
    }
  }
  .nav {
    width: 70%;
    ul {
      li {
        color: #af8f0b;
        font-size: clamp(1rem, 1.4vw, 1.5rem);
        &:hover {
          color: #796206;
        }

        button {
          background: #f1c40f;
        }
        button:hover {
          background-color: #dcb51c;
        }
      }
    }
  }
}
.contacte {
  cursor: pointer;
}
.hover-el {
  position: fixed;
  z-index: 40;
  width: 25%;
  display: flex;
  flex-flow: row wrap;
  left: 50%;
  box-shadow: 0px 0 1px rgba(0, 0, 0, 0.3);
  top: 7%;
  transition: All 0.3s;
  background: #f1f1f1;
  ul {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
    padding: 30px 0;
    li {
      width: 50%;
      display: flex;
      flex-flow: column wrap;
      justify-content: center;
      align-items: center;
      font-weight: bold;
      font-size: 0.8rem;
      margin-bottom: 10px;
      &:hover {
        transform: scale(1.1);
        transition: All 0s;
      }
      img {
        width: 25px;
        margin: 0 auto;
      }
    }
  }
}
.list-enter {
  transform: translate3d(0, -30px, 0);
  opacity: 0;
}
.list-enter-to {
  transform: translate3d(0, 0, 0);
  opacity: 1;
}
.list-leave {
  transform: translate3d(0, 0, 0);
  opacity: 1;
}
.list-leave-to {
  transform: translate3d(0, -30px, 0) scale(0.5);
  opacity: 0;
}
.mobile {
  .mobile-list {
    position: absolute;
    top: 0;
    right: 0;
    width: 30%;
    height: 100vh;
    display: flex;
    flex-flow: column wrap;
    align-items: center;
    justify-content: flex-start;
    text-align: center;
    z-index: 30;
    background: #f1f1f1;
    @media (max-width: 426px) {
      width: 50%;
    }
    .button {
      margin: 0;
    }
  }
}
.cross {
  background: #f1f1f1;
}

.list-mobile-enter-active,
.list-mobile-leave-active {
  transform: translate(0%, 0);
  transition: All 0.3s;
}
.list-mobile-leave-to /* .fade-leave-active below version 2.1.8 */ {
  transform: translate(100%, 0);
  transition: All 0.3s;
}
.list-mobile-enter {
  transform: translate(100%, 0);
  transition: All 0.3s;
}
</style>