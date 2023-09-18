<template>
  <section>
    <div class="video-container">
      <video autoplay muted loop playsinline>
        <source src="../assets/videos/banner.mp4" type="video/mp4" />
      </video>
    </div>
    <div class="video-clone">
      <div class="text-container-front">
        <h1>SINTA ESTÁ VIBRAÇÃO</h1>
      </div>
    </div>
    <div class="text-container-back">
      <h1>SINTA ESTÁ VIBRAÇÃO</h1>
    </div>
  </section>
</template>

<script>
export default {
  name: "PvBanner",
};
</script>

<style scoped lang="scss">
section {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 150px;
  margin-bottom: 60px;
  width: 100%;
  position: relative;

  @media (min-width: 769px) {
    margin-top: 200px;
  }

  h1 {
    font-size: 24px;
    font-weight: 600;
  }

  .video-container {
    width: inherit;
    max-width: 800px;
    max-height: 800px;
    z-index: 2;

    video {
      width: inherit;
      max-width: inherit;
      max-height: inherit;
      object-fit: cover;
    }
  }

  .video-clone {
    top: 0;
    position: absolute;
    width: 100%;
    max-height: 800px;
    height: 100%;
    z-index: 3;
    -webkit-clip-path: inset(0);
    clip-path: inset(0);
    clip: rect(0px, auto, auto, 0px);

    .text-container-front {
      width: 100%;
      height: calc(100% + 60px);

      top: 0;
      position: absolute;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-end;

      h1 {
        font-size: 24px;
        position: sticky;
        bottom: 5rem;
        color: $black;

        @media (min-width: 769px) {
          font-size: 32px;
        }
        @media (min-width: 1500px) {
          bottom: 12rem;
          font-size: 48px;
        }
      }
    }
  }
  .text-container-back {
    width: 100%;
    height: calc(100% + 60px);

    top: 0;
    position: absolute;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-end;

    h1 {
      position: sticky;
      bottom: 5rem;
      @media (min-width: 769px) {
        font-size: 32px;
      }
      @media (min-width: 1500px) {
        bottom: 12rem;
        font-size: 48px;
      }
    }
  }
}
</style>
