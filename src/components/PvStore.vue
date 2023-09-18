<template>
  <section>
    <div class="video-container">
      <video autoplay muted loop playsinline>
        <source src="../assets/videos/store.mp4" type="video/mp4" />
      </video>
    </div>
    <div class="video-clone">
      <div class="text-container-front">
        <h1>Venha Vibrar com agente</h1>
      </div>
    </div>
    <div class="text-container-back">
      <h1>Venha Vibrar com agente</h1>
    </div>
  </section>
</template>

<script>
export default {
  name: "PvStore",
};
</script>

<style scoped lang="scss">
section {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0 auto;
  margin-top: 80px;
  width: 100%;
  position: relative;
  max-width: 1250px;

  h1 {
    font-size: 24px;
    font-weight: 600;
    text-transform: uppercase;
    padding: 0 40px;
    text-align: center;
  }

  .video-container {
    width: inherit;
    height: 80vh;
    z-index: 2;

    video {
      width: inherit;
      height: inherit;
      object-fit: cover;
      filter: contrast(0.7);
      box-shadow: inset 0px 0px 40px 40px #dba632;
    }
  }

  .video-clone {
    top: 0;
    position: absolute;
    width: 100%;
    height: 100%;
    z-index: 3;
    -webkit-clip-path: inset(0);
    clip-path: inset(0);
    clip: rect(0px, auto, auto, 0px);

    .text-container-front {
      z-index: 4;
      width: 100%;
      height: calc(100% + 130px);
      top: 0;
      position: absolute;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-end;

      h1 {
        font-size: 24px;
        position: sticky;
        top: 50%;
        bottom: 2rem;
        color: $black;

        @media (min-width: 769px) {
          font-size: 32px;
        }
      }
    }
  }
  .text-container-back {
    width: 100%;
    height: calc(100% + 130px);

    top: 0;
    position: absolute;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-end;

    h1 {
      position: sticky;
      bottom: 2rem;

      @media (min-width: 769px) {
        font-size: 32px;
      }
      @media (min-width: 1500px) {
        font-size: 48px;
      }
    }
  }
}
</style>
