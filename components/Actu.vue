<template>
  <div>
    <div class="conteneur flex flex-col justify-center align-center">
      <h1 class="text-xl md:text-2xl lg:text-4xl font-bold text-center">
        Retrouvez toute notre actualité
      </h1>
      <hr />
      <div class="mx-auto">
        <a
          href="https://www.linkedin.com/company/experts-du-montage/?originalSubdomain=fr"
          ><button
            class="button-etape hover:bg-yellow-600 mt-10 rounded px-4 py-2 text-sm font-bold leading-6 text-center text-white transition shadow focus:outline-none hover:shadow-lg md:text-2xl"
          >
            Linked <i class="fab fa-linkedin"></i>
          </button>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang='scss'>
h1 {
  font-family: "M PLUS Rounded 1c", sans-serif;
}
.conteneur {
  height: 500px;
  @media (max-width: 425px) {
    height: 300px;
  }
}
hr {
  width: 10%;
  color: gray;
  margin: 0 auto;
  border: 1px solid gray;
  background: gray;
  margin-top: 15px;
}
.button-etape {
  background: #21327d;
  color: white;
}
.button-etape:hover {
  background: #18245b;
}
</style>