<template>
  <div>
    <Banniere class="mb-20" />
    <Slider class="mb-32" />
    <Etape />
    <Confiance />
    <Perceuse />
    <Carte />
    <Actu />
  </div>
</template>

<script>
import Banniere from "../components/Banniere";
import Slider from "../components/Slider";
import Etape from "../components/Etape";
import Confiance from "../components/Confiance";
import Perceuse from "../components/Perceuse";
import Carte from "../components/Carte";
import Actu from "../components/Actu";

export default {
  components: { Confiance },
  component: {
    Banniere,
    Slider,
    Etape,
    Confiance,
    Perceuse,
    Carte,
    Actu,
  },
};
</script>

<style lang="scss">
</style>
