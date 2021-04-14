<template>
  <div class="relative conteneur-principal mt-32 h-screen">
    <div
      class="h-screen fond flex justify-between lg:p-32 items-center bg-yellow-500"
    >
      <img class="img2" src="form1.svg" alt="" />
      <img class="img1" src="like.svg" alt="" />
    </div>
    <div
      class="conteneur-text absolute top-0 left-0 w-full flex-col h-full flex justify-center items-center"
    >
      <h1
        class="w-4/6 titre text-black text-xl md:text-3xl lg:text-5xl font-bold lg:w-1/2 text-center mb-6"
      >
        Vous êtes monteur professionnel de mobilier ?
      </h1>
      <p
        class="w-5/6 text-black text-center text-lg md:text-xl lg:text-3xl lg:w-1/2 mb-6"
      >
        Vous souhaitez rejoindre la communauté des Experts du Montage ?
      </p>
      <p
        class="w-5/6 lg:w-1/3 text-black text-center text-lg md:text-xl lg:text-3xl mb-10"
      >
        Pour que nous puissions travailler ensemble, merci de compléter le
        questionnaire ci-dessous.
      </p>
      <a
        href="https://docs.google.com/forms/d/e/1FAIpQLSczCOlSmzdP2fQSzAIBrKvJEfInJkvhC8BWz02Dzpf8uHrQLQ/viewform"
      >
        <button
          class="px-4 py-2 lg:px-16 lg:py-6 font-bold text-md lg:text-2xl font-medium leading-6 text-center text-yellow-500 uppercase transition bg-blue-600 shadow focus:outline-none hover:shadow-lg hover:bg-blue-700"
        >
          REMPLIR LE FORMULAIRE
        </button></a
      >
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang='scss'>
.conteneur-principal {
  width: 100%;
}
.img1 {
  width: 200px;
  position: relative;
  z-index: 20;
  @media (max-width: 1024px) {
    width: 100px;
  }
  @media (max-width: 768px) {
    width: 66px;
    top: 40%;
    right: calc(50% - 33px);
  }
}

.img2 {
  width: 200px;
  position: relative;
  z-index: 20;
  @media (max-width: 1024px) {
    width: 100px;
  }
  @media (max-width: 768px) {
    width: 66px;
    top: -40%;
    left: calc(50% - 33px);
  }
}
.titre {
  line-height: 3.5rem;
  @media (max-width: 768px) {
    line-height: 1.7rem;
  }
}
.conteneur-text {
  line-height: 2.5rem;
  z-index: 5;
  @media (max-width: 768px) {
    line-height: 1.7rem;
  }
}

.fond:after {
  position: absolute;
  bottom: 0;
  right: 0;
  content: "";
  height: 100%;
  width: 100%;
  clip-path: polygon(50% 100%, 100% 0%, 100% 100%);
  background-color: #394888;
  @media (max-width: 768px) {
    display: none;
  }
}

p {
  font-family: "M PLUS Rounded 1c", sans-serif;
}
</style>