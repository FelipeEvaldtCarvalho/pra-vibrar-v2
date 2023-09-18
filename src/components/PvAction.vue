<template>
  <section>
    <a class="btn bg-white c-black" href="">LOJA VIRTUAL</a>
  </section>
</template>
<script>
export default {
  name: "PvAction",
};
</script>

<style scoped lang="scss">
section {
  width: 100%;
  max-width: 1250px;
  margin: auto;
  height: 200px;
  background-image: url("../assets/images/action.png");
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  align-items: center;
  justify-content: center;

  @media (min-width: 769px) {
    height: 400px;
  }
}
</style>
