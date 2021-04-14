<template>
  <div class="mt-20">
    <h1
      class="titre-principal text-xl md:text-2xl lg:text-4xl font-bold text-center p-20"
    >
      ILS NOUS FONT CONFIANCE
    </h1>
    <div class="flex flex-row justify-center flex-wrap conteneur-principal">
      <div class="conteneur">
        <img class="logo" src="logo/asetam.png" alt="logo asetam" />
      </div>
      <div class="conteneur">
        <img class="logo" src="logo/chalet.png" alt="logo chaletdejardin.fr" />
      </div>
      <div class="conteneur">
        <img class="logo" src="logo/desk.png" alt="logo bemyDesk" />
      </div>
      <div class="conteneur">
        <img class="logo" src="logo/espacebureau.png" alt="logo EspaceBureau" />
      </div>
      <div class="conteneur">
        <img class="logo" src="logo/leroy-merlin.png" alt="logo leroyMerlin" />
      </div>
      <div class="conteneur">
        <img class="logo" src="logo/letaneur.png" alt="logo le tanneur" />
      </div>
      <div class="conteneur">
        <img class="logo" src="logo/mibibam.jpg" alt="logo mobibam" />
      </div>
      <div class="conteneur black">
        <img class="logo" src="logo/mob.png" alt="logo mob-mob.fr" />
      </div>
      <div class="conteneur">
        <img class="logo" src="logo/permanence.png" alt="logo la permanence" />
      </div>
      <div class="conteneur">
        <img class="logo" src="logo/pickawood.png" alt="logo pickawood" />
      </div>

      <div class="conteneur">
        <img class="logo" src="logo/sephora.png" alt="logo sephora" />
      </div>
      <div class="conteneur black">
        <img class="logo" src="logo/tikimob.jpg" alt="logo tikimob.fr" />
      </div>
      <div class="conteneur">
        <img
          class="logo"
          src="
              logo/zara.jpg"
          alt="logo zara"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang='scss'>
.titre-principal {
  color: #9f9f9f;
  position: relative;
}
.titre-principal:before {
  content: "";
  height: 3px;
  width: 20%;
  background: #f2b600;
  position: absolute;
  top: 108px;
  left: 10%;
  border-radius: 50%;
  @media (max-width: 768px) {
    top: 93px;
    width: 10%;
  }
  @media (min-width: 768px) {
    top: 93px;
    width: 10%;
  }
  @media (min-width: 1024px) {
    top: 93px;
    width: 10%;
  }
}
.titre-principal:after {
  content: "";
  height: 3px;
  width: 20%;
  background: #f2b600;
  position: absolute;
  top: 108px;
  left: 70%;
  border-radius: 50%;
  @media (max-width: 768px) {
    top: 93px;
    width: 10%;
    left: 80%;
  }
  @media (min-width: 768px) {
    top: 93px;
    width: 10%;
    left: 80%;
  }
  @media (min-width: 1024px) {
    top: 93px;
    width: 10%;
    left: 80%;
  }
}
.conteneur {
  width: 175px;
  height: 175px;
  border-radius: 50%;
  background: white;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 2px 2px 4px rgb(128, 128, 128);
  margin: 20px 30px;
  transition: 0.2s all;
  user-select: none;
  @media (max-width: 768px) {
    width: 100px;
    height: 100px;
  }
  @media (max-width: 480px) {
    width: 60px;
    height: 60px;
    margin: 10px 15px;
  }
}
.conteneur:hover {
  transform: scale(1.05);
}
.logo {
  width: 100px;
  pointer-events: none;
  @media (max-width: 768px) {
    width: 70px;
  }
  @media (max-width: 480px) {
    width: 40px;
  }
}
.black {
  background: black;
}
</style>