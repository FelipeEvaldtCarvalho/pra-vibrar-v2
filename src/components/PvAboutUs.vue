<template>
  <section>
    <div class="text-container">
      <h1>Quem somos</h1>
      <p class="c-gray">
        Somos a maior <span class="c-white">SEX SHOP</span> da região, que tem
        como propósito oferecer um atendimento descomplicado, leve, pautado pelo
        respeito às diferenças e necessidades de cada cliente, com diversidade
        de sex toys, cosméticos e lingeries.
      </p>
    </div>
    <img src="../assets/images/about.png" alt="" />
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
  max-width: 1200px;
  margin: auto;
  position: relative;

  img {
    display: none;

    @media (min-width: 769px) {
      display: block;
      position: absolute;
      right: 0;
      top: 0;
      bottom: 0;
      margin: auto 0;
      width: 30%;
    }
  }

  .text-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 0 40px;
    text-align: center;
    gap: 1rem;

    @media (min-width: 769px) {
      margin: 9rem auto;
      gap: 2rem;
    }

    h1 {
      font-size: 24px;
      font-weight: 600;
      text-transform: uppercase;
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
        width: 65%;
        font-size: 26px;
        align-self: flex-start;
        text-align: left;
      }
      @media (min-width: 1500px) {
      }
    }
  }
}
</style>
