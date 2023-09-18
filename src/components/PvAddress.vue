<template>
  <section>
    <p class="c-gray">
      Sinta a qualidade dos nossos produtos em primeira mão, visite nossa loja!
    </p>
    <ion-icon name="location-sharp"></ion-icon>
    <p>Av. General Flores da Cunha, 4489 Pda 59 - Cachoeirinha - RS</p>
    <p class="c-gray">
      Te esperamos em nossa loja de segunda a sexta das 10h as 20h aos sábados
      das 10h as 19h
    </p>
    <a class="btn c-black bg-white w-100" href="">VENHA</a>
  </section>
</template>

<script>
export default {
  name: "PvAddress",
};
</script>

<style scoped lang="scss">
section {
  margin: auto;
  margin-top: 130px;
  padding: 40px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 2rem;
  text-align: center;
  max-width: 1200px;

  @media (min-width: 769px) {
    gap: 3rem;
    margin-bottom: 130px;
  }

  ion-icon {
    font-size: 25px;

    @media (min-width: 769px) {
      font-size: 48px;
    }
  }

  p {
    font-size: 16px;
    font-weight: 300;

    @media (min-width: 769px) {
      font-size: 24px;
    }
  }

  .btn {
    @media (min-width: 769px) {
      width: 195px;
    }
  }
}
</style>
