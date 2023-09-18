<template>
  <section>
    <div
      v-for="(category, index) in categories"
      v-bind:key="index"
      v-bind:class="`category-item ${
        index === activeCategorie ? 'active' : 'inactive'
      }`"
    >
      <div
        class="image-container"
        :ref="`image_container_${category.class}`"
        @click="activeCategorie = index"
      >
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
export default {
  name: "PvCategories",
  data() {
    return {
      windowWidth: 0,
      activeCategorie: 0,
      activeAnimateDuration: 1,
      inactiveAnimateDuration: 1,
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
    handleResize() {
      this.windowWidth = window.innerWidth;
    },
  },
  mounted() {
    window.addEventListener("resize", this.handleResize);
    this.handleResize();
  },
};
</script>

<style scoped lang="scss">
section {
  padding: 40px;
  width: 100%;
  max-width: 1250px;
  margin: auto;
  display: flex;
  flex-direction: column;
  gap: 2rem;

  * {
    transition: 0.5s all ease;
  }

  @media (min-width: 769px) {
    flex-direction: row;
    justify-content: space-between;
    gap: 0;
  }
  .category-item {
    display: flex;
    flex-direction: column;
    gap: 2rem;

    @media (min-width: 769px) {
      width: 13%;
    }

    .text {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      height: 0;
      overflow: hidden;
      opacity: 0;

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
      cursor: pointer;

      @media (min-width: 769px) {
        height: 50vw;
        max-height: 500px;
        width: 100%;
        align-items: end;
      }

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
        @media (min-width: 769px) {
          word-break: break-all;
          font-size: 2vw;
        }
        @media (min-width: 769px) {
          word-break: break-all;
          font-size: 2vw;
        }
        @media (min-width: 1440px) {
          word-break: break-all;
          font-size: 29px;
        }
      }
    }
  }
  .active {
    @media (min-width: 769px) {
      width: 50%;
      max-width: auto;
    }
    .text {
      height: auto;
      overflow: initial;
      opacity: 1;
      h1 {
        @media (min-width: 769px) {
          font-size: 2vw;
        }
        @media (min-width: 1440px) {
          font-size: 29px;
        }
      }
      p {
        @media (min-width: 1440px) {
          font-size: 24px;
        }
      }
    }
    .image-container {
      aspect-ratio: 1 / 1;

      img {
        filter: none;
      }

      &__inner-title {
        opacity: 0;
      }
    }
  }
}
</style>
