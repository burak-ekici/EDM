<template>
  <div class="footer pt-16 justify-center flex flex-col md:flex-row flex-wrap">
    <!-- section 1 du footer  -->
    <div class="col1 w-full text-center mb-8 p-8 md:pl-16">
      <div>
        <img class="mx-auto" src="/logo.png" alt="" />
      </div>
      <div class="text-white pt-6 lg:w-2/3 lg:mx-auto">
        <p class="font-bold">
          EXPERTS DU MONTAGE est LE service de pose de mobilier en B2B, qui
          travaille sur l'ensemble de la France et tout le Bénélux francophone.
        </p>
        <p class="pt-4">
          Nous travaillons avec de nombreux fournisseurs de mobilier et de
          rayonnages, des agenceurs, des architectes d’intérieurs et des
          revendeurs régionaux. Nous gérons la pose et le montage de leurs
          produits directement chez leurs clients.
        </p>
        <p class="pt-4">
          Pour ces interventions, nous faisons intervenir des partenaires
          professionnels locaux, spécialisés dans le montage de mobilier, notés
          et recommandés par nos clients.
        </p>
      </div>
    </div>
    <!-- section 2 du footer  -->
    <div class="col2 md:w-1/2 p-8 md:pl-16 text-white mt-8">
      <h1 class="text-center text-2xl -mt-8 lg:mt-0 mb-4 lg:mb-20">
        Liens utiles
      </h1>
      <ul class="flex items-center justify-center flex-col text-4xl">
        <li>
          <a href="https://www.youtube.com/channel/UCIc5eo1bIXo8dHxEqRZS_Qw"
            ><i class="fab fa-youtube"></i
          ></a>
        </li>
        <li>
          <a
            href="https://www.linkedin.com/company/experts-du-montage/?originalSubdomain=fr"
            ><i class="fab fa-linkedin"></i
          ></a>
        </li>
      </ul>
    </div>
    <!-- section 3 du footer  -->
    <div
      class="col3 md:w-1/2 p-8 md:pl-16 text-white flex flex-col items-center"
    >
      <h1 class="text-xl mb-2 font-semibold">Projet soutenu par</h1>
      <img src="soutenue-par.png" alt="logo sponsor bpifrance" />
      <p class="mt-6">Nous contacter au :</p>
      <p class="font-bold">
        <i class="fas fa-phone-alt mr-2 text-green-500 text-2xl"></i>07 78 45 68
        32
      </p>
      <p class="mt-6">Ou par mail à l'adresse : <br /></p>
      <p class="font-bold">contact@expertsdumontage.com</p>
    </div>
    <p class="block w-full text-xs pb-2 text-center copyright">
      © CP 2021 Experts du montage | Tous droits réversés | Privacy Policy
    </p>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
.footer {
  background: #3a4888;

  font-family: "M PLUS Rounded 1c", sans-serif;
  div:nth-child(1) {
    img {
      filter: contrast(150%);
    }
  }
  .fa-youtube {
    color: #ff0000;
  }
  .fa-linkedin {
    color: #0a66c2;
  }
}
.copyright {
  background: #3a4888;
  color: white;
}
</style>