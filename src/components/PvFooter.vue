<template>
  <footer>
    <a href="">
      <img :src="require('@/assets/images/logo.png')" alt="Logo" />
    </a>
    <div class="list contact">
      <span class="list__item--icon">
        <ion-icon class="c-gray" name="call"></ion-icon>
        <p class="c-gray">(51) 989 304 355</p>
      </span>
      <a href="">
        <span class="list__item--icon">
          <ion-icon class="c-gray" name="storefront"></ion-icon>
          <p class="c-gray">www.pravibrar.com.br</p>
        </span></a
      >
      <span class="list__item--icon">
        <ion-icon class="c-gray" name="mail"></ion-icon>
        <p class="c-gray">pravibrarsexshop@gmail.com</p>
      </span>
    </div>
    <div class="list">
      <p class="c-gray">© Pra Vibrar - Sex Shop</p>
      <p class="c-gray">2023 Todos os direitos reservados.</p>
      <p class="c-gray">CNPJ: 25.121.144/0001-27</p>
    </div>
  </footer>
</template>

<script>
export default {
  name: "PvFooter",
};
</script>

<style lang="scss" scoped>
footer {
  display: flex;
  flex-direction: column;
  gap: 3rem;
  padding: 40px;
  align-items: center;

  @media (min-width: 769px) {
    justify-content: space-between;
    flex-direction: row;
  }

  a {
    text-decoration: none;
  }

  img {
    height: 100px;
  }

  .list {
    display: flex;
    flex-direction: column;
    font-size: 15px;
    text-align: center;
    min-width: 29vw;
    align-items: center;
    letter-spacing: 0.3vw;
    gap: 1rem;

    a,
    &__item--icon {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1rem;
      margin-bottom: 0.6vw;

      @media (min-width: 769px) {
        margin-bottom: 8px;
        gap: 0.5rem;
        flex-direction: row;
        align-self: flex-start;
      }

      ion-icon {
        font-size: 25px;
      }
    }
  }
}
</style>
