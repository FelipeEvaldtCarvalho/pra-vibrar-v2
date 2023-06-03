<template>
  <section>
    <div
      v-for="(category, index) in categories"
      v-bind:key="index"
      @click="activeCategorie = index"
      class="category-item"
    >
      <div class="image-container" :ref="`image_container_${category.class}`">
        <img
          :ref="`image_${category.class}`"
          :src="require(`@/assets/images/${category.img}`)"
          alt=""
        />
        <h1
          class="image-container__inner-title"
          :ref="`inner_title_${category.class}`"
        >
          {{ category.title }}
        </h1>
      </div>
      <div class="text" :ref="`text_${category.class}`">
        <h1>{{ category.title }}</h1>
        <p class="c-gray">{{ category.text }}</p>
      </div>
    </div>
  </section>
</template>

<script>
import { gsap } from "gsap";
export default {
  name: "PvCategories",
  data() {
    return {
      activeCategorie: 0,
      activeAnimateDuration: 1,
      inactiveAnimateDuration: 0.5,
      categories: [
        {
          title: "Vibradores",
          text: "Descubra novas texturas, tamanhos, formatos e sensações.",
          class: "vibs",
          img: "vibs.png",
        },
        {
          title: "BDSM",
          text: "Liberte sua imaginação, seja quem quiser, escolha dominar ou se submeter.",
          class: "bdsm",
          img: "bdsm.png",
        },
        {
          title: "Acessórios",
          text: "Não há limites para a imaginação, experiemente, saia da rotina.",
          class: "acessory",
          img: "acessories.png",
        },
        {
          title: "Cosméticos",
          text: "Eleve sua experiência com a nossa linha de cosméticos  de alta qualidade.",
          class: "cosmetics",
          img: "cosmetics.png",
        },
      ],
    };
  },
  methods: {
    init() {
      gsap.set(this.$refs.image_container_vibs, { aspectRatio: "1 / 1" });
      gsap.set(this.$refs.image_vibs, { filter: "none" });
      gsap.set(this.$refs.inner_title_vibs, { opacity: 0 });
      gsap.set(this.$refs.text_vibs, {
        display: "flex",
        flexDirection: "column",
        gap: "1rem",
      });
      console.log(this.$refs);
    },
    active(elementClass) {
      const elementImageContainer =
        this.$refs[`image_container_${elementClass}`];
      const elementImage = this.$refs[`image_${elementClass}`];
      const elementInnerTitle = this.$refs[`inner_title_${elementClass}`];
      const elementText = this.$refs[`text_${elementClass}`];
      gsap.fromTo(
        elementImageContainer,
        { aspectRatio: "5 / 1" },
        { aspectRatio: "1 / 1", duration: this.activeAnimateDuration }
      );
      gsap.fromTo(
        elementImage,
        { filter: "saturate(0) contrast(0.5)" },
        { filter: "none", duration: this.activeAnimateDuration }
      );
      gsap.fromTo(
        elementInnerTitle,
        { opacity: 1 },
        { opacity: 0, duration: this.activeAnimateDuration }
      );
      gsap.fromTo(
        elementText,
        { display: "none" },
        {
          display: "flex",
          flexDirection: "column",
          gap: "1rem",
          duration: this.activeAnimateDuration,
        }
      );
    },
    inactive(elementClass) {
      const elementImageContainer =
        this.$refs[`image_container_${elementClass}`];
      const elementImage = this.$refs[`image_${elementClass}`];
      const elementInnerTitle = this.$refs[`inner_title_${elementClass}`];
      const elementText = this.$refs[`text_${elementClass}`];
      gsap.fromTo(
        elementImageContainer,
        { aspectRatio: "1 / 1" },
        { aspectRatio: "5 / 1", duration: this.inactiveAnimateDuration }
      );
      gsap.fromTo(
        elementImage,
        { filter: "none" },
        {
          filter: "saturate(0) contrast(0.9) brightness(0.7)",
          duration: this.inactiveAnimateDuration,
        }
      );
      gsap.fromTo(
        elementInnerTitle,
        { opacity: 0 },
        { opacity: 1, duration: this.inactiveAnimateDuration }
      );
      gsap.fromTo(
        elementText,
        { display: "flex" },
        { display: "none", duration: 0.2 }
      );
    },
  },
  watch: {
    activeCategorie(newValue, oldValue) {
      const oldActive = this.categories[oldValue].class;
      const newActive = this.categories[newValue].class;
      this.active(newActive);
      this.inactive(oldActive);
    },
  },
  mounted() {
    this.init();
  },
};
</script>

<style scoped lang="scss">
section {
  padding: 40px;
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 2rem;
  .category-item {
    display: flex;
    flex-direction: column;
    gap: 2rem;
    .text {
      display: none;
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
    .image-container {
      display: flex;
      align-items: center;
      padding: 20px;
      position: relative;
      width: 100%;
      height: 100%;
      aspect-ratio: 5 / 1;

      img {
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
        object-fit: cover;
        align-self: start;
        filter: saturate(0) contrast(0.9) brightness(0.7);
      }

      &__inner-title {
        text-transform: uppercase;
        font-size: 24px;
        z-index: 2;
      }
    }
  }
}
</style>
