<template>
  <footer>
    <img :src="require('@/assets/images/logo.png')" alt="Logo" />
    <div class="list">
      <span class="list__item--icon">
        <ion-icon class="c-gray" name="call"></ion-icon>
        <p class="c-gray">(51) 989 304 355</p>
      </span>
      <span class="list__item--icon">
        <ion-icon class="c-gray" name="storefront"></ion-icon>
        <p class="c-gray">www.pravibrar.com.br</p>
      </span>
      <span class="list__item--icon">
        <ion-icon class="c-gray" name="mail"></ion-icon>
        <p class="c-gray">pravibrarsexshop@gmail.com</p>
      </span>
      <div>
        <p class="c-gray">© Pra Vibrar - Sex Shop</p>
        <p class="c-gray">2023 Todos os direitos reservados.</p>
        <p class="c-gray">CNPJ: 25.121.144/0001-27</p>
      </div>
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

    &__item--icon {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1rem;
      margin-bottom: 0.6vw;

      ion-icon {
        font-size: 25px;
      }
    }
  }
}
</style>
