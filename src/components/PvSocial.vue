<template>
  <section>
    <h1>conheça melhor nossa loja</h1>
    <a class="btn bg-white social w-100">
      <ion-icon class="c-black" name="logo-instagram"></ion-icon>
      <p class="c-black">Nosso Instagram</p>
    </a>
    <a class="btn bg-white c-black social w-100">
      <ion-icon class="c-black" name="logo-whatsapp"></ion-icon>
      <p class="c-black">Fale com a gente</p>
    </a>
  </section>
</template>

<script>
export default {
  name: "PvSocial",
};
</script>

<style scoped lang="scss">
section {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  padding: 0 40px;
  gap: 2rem;

  @media (min-width: 769px) {
    gap: 3rem;
    margin-bottom: 4rem;
  }

  h1 {
    font-size: 24px;
    text-transform: uppercase;
    text-align: center;
    font-weight: 700;

    @media (min-width: 769px) {
      font-size: 32px;
    }
    @media (min-width: 1500px) {
      font-size: 48px;
    }
  }
  .social {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 11px;

    @media (min-width: 769px) {
      flex-direction: row;
      justify-content: center;
    }

    ion-icon {
      font-size: 25px;
    }
    p {
      text-transform: uppercase;
      font-weight: 700;
      font-size: 14px;
    }
  }
  .btn {
    cursor: pointer;
    @media (min-width: 769px) {
      width: 350px;
      text-align: center;
    }
  }
}
</style>
