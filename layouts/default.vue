<template>
  <div>
    <v-app>
      <div class="w-full overflow-hidden">
        <div class="mb-32 toolbar">
          <Navbar2 />
        </div>
        <Nuxt />
        <div>
          <Footer />
        </div>
      </div>
    </v-app>
  </div>
</template>

<script>
import Navbar2 from "../components/Navbar2";
import Footer from "../components/Footer";
export default {
  components: {
    Navbar2,
    Footer,
  },
};
</script>

<style scoped lang="scss">
html,
body,
* {
  color: #444b54;
}
.toolbar {
  transition: All 0.7s;
}
</style>
