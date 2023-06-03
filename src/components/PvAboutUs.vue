<template>
  <section>
    <h1>Quem somos</h1>
    <p class="c-gray">
      Somos a maior <span class="c-white">SEX SHOP</span> da região, que tem
      como propósito oferecer um atendimento descomplicado, leve, pautado pelo
      respeito às diferenças e necessidades de cada cliente, com diversidade de
      sex toys, cosméticos e lingeries.
    </p>
  </section>
</template>
<script>
export default {
  name: "PvAboutUs",
};
</script>

<style scoped lang="scss">
section {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 0 40px;
  text-align: center;
  gap: 1rem;

  h1 {
    font-size: 24px;
    font-weight: 600;
    text-transform: uppercase;
  }
  p {
    font-size: 16px;
    font-weight: 300;
  }
}
</style>
