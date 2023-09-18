<template>
  <section>
    <div class="text-container">
      <p>
        Aqui na <span class="c-white">Pra Vibrar</span>, provocamos nosso
        público a explorar suas fantasias de uma forma livre e desconstruída.
        Vibração é energia e nós trabalhamos pra te ver
        <span class="c-white">VIBRAR</span>!
      </p>
      <img :src="require('@/assets/images/banner.png')" alt="" />
    </div>
  </section>
</template>

<script>
export default {
  name: "PvBannerText",
};
</script>

<style scoped lang="scss">
section {
  width: 100%;
  padding: 1.5rem 0;
  max-width: 1200px;
  margin: 0 auto;

  .text-container {
    width: inherit;
    margin: 0 auto;
    display: flex;
    flex-direction: column;

    @media (min-width: 769px) {
      flex-direction: row;
      align-items: center;
    }

    p {
      font-size: 16px;
      font-weight: 300;
      text-align: center;
      color: $gray;
      padding: 0 40px;
      padding-bottom: 2rem;

      @media (min-width: 769px) {
        font-size: 24px;
        text-align: left;
      }
    }

    img {
      width: 100%;
      object-fit: cover;
      @media (min-width: 769px) {
        width: 40%;
      }
    }
  }
}
</style>
