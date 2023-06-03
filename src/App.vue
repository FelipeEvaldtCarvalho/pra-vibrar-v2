<template>
  <PvNavbar />
  <pv-banner />
  <pv-banner-text />
  <pv-action />
  <pv-text />
  <pv-categories />
  <pv-about-us />
</template>

<script>
import PvAboutUs from "./components/PvAboutUs.vue";
import PvAction from "./components/PvAction.vue";
import PvBanner from "./components/PvBanner.vue";
import PvBannerText from "./components/PvBannerText.vue";
import PvCategories from "./components/PvCategories.vue";
import PvNavbar from "./components/PvNavbar.vue";
import PvText from "./components/PvText.vue";

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
