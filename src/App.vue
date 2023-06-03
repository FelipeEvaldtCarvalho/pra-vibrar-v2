<template>
  <PvNavbar />
  <pv-banner />
  <pv-banner-text />
  <pv-action />
  <pv-text />
  <pv-categories />
  <pv-about-us />
  <pv-store />
  <pv-address />
  <pv-social />
  <pv-footer />
</template>

<script>
import PvAboutUs from "./components/PvAboutUs.vue";
import PvAction from "./components/PvAction.vue";
import PvAddress from "./components/PvAddress.vue";
import PvBanner from "./components/PvBanner.vue";
import PvBannerText from "./components/PvBannerText.vue";
import PvCategories from "./components/PvCategories.vue";
import PvNavbar from "./components/PvNavbar.vue";
import PvStore from "./components/PvStore.vue";
import PvText from "./components/PvText.vue";
import PvSocial from "./components/PvSocial.vue";
import PvFooter from "./components/PvFooter.vue";

export default {
  name: "App",
  components: {
    PvNavbar,
    PvBanner,
    PvBannerText,
    PvAction,
    PvText,
    PvCategories,
    PvAboutUs,
    PvStore,
    PvAddress,
    PvSocial,
    PvFooter,
  },
};
</script>

<style lang="scss">
* {
  font-family: "Montserrat", sans-serif;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  color: $white;
}
body {
  background-color: #000;
}
</style>
