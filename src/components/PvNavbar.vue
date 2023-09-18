<template>
  <nav ref="nav">
    <ion-icon name="location"></ion-icon>
    <img :src="require(`@/assets/images/logo.png`)" ref="logo" />
    <ion-icon name="storefront"></ion-icon>
  </nav>
</template>

<script>
export default {
  name: "PvNavbar",
  data() {
    return {
      scrollPosition: 0,
    };
  },
  computed: {
    smallLogo() {
      return this.scrollPosition > 10;
    },
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);
  },
  unmounted() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.scrollPosition = window.scrollY;
    },
  },
  watch: {
    scrollPosition(newPosition, oldPostion) {
      if (newPosition > 50) {
        this.$refs.logo.style.height = "50px";
      } else {
        this.$refs.logo.style.height = "35vw";
      }

      if (oldPostion < newPosition && newPosition > 50) {
        this.$refs.nav.style.opacity = 0;
      }
      if (oldPostion > newPosition) {
        this.$refs.nav.style.opacity = 1;
      }
    },
  },
};
</script>

<style scoped lang="scss">
nav {
  transition: 0.6s ease all;
  display: flex;
  padding: 1rem;
  justify-content: space-between;
  border-bottom: none;
  position: fixed;
  top: 0;
  left: 0;
  background-color: $black;
  width: 100%;
  z-index: 100;
  border-bottom: 1px $white solid;

  @media (min-width: 1440px) {
    justify-content: space-around;
  }

  ion-icon {
    font-size: 2rem;
    cursor: pointer;
  }

  img {
    transition: 0.6s ease all;
    min-height: 50px;
    height: 35vw;
    max-height: 150px;
    cursor: pointer;
  }
}
</style>
