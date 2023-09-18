<template>
  <section>
    <h1>DESCUBRA NOVAS FORMAS DE PRAZER</h1>
    <p class="c-gray">
      Prazer livre e desconstruído só aqui na
      <span class="c-white">Pra Vibrar</span> oferecemos uma enorme variedade de
      brinquedinhos, lingeries, cosméticos, itens de cuidados íntimos, BDSM &
      muitoooo mais!
    </p>
  </section>
</template>

<script>
export default {
  name: "PvText",
};
</script>

<style scoped lang="scss">
section {
  padding: 40px;
  display: flex;
  flex-direction: column;
  gap: 37px;
  text-align: center;
  max-width: 1200px;
  margin: auto;

  @media (min-width: 769px) {
    gap: 5rem;
    margin: 5% auto;
  }

  h1 {
    font-size: 24px;
    font-weight: 600;

    @media (min-width: 769px) {
      font-size: 32px;
    }
    @media (min-width: 1500px) {
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
}
</style>
