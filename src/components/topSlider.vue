<template>
  <div class="top-slider pt-3 border">

    <router-link
    to="/about"
    class="top-slider__slide t-center rounded-xl bg-black ratio-4x3 py-3 px-2"
    >
      <img
      src="/assets/img/top-slider/SfyXGMjOp0c 1.png"
      class="top-slider__bg-img img-cover"
      alt="TODO"
      >

      <div class="top-slider__text t-white">
        <h3 class="top-slider__subtitle">О КЛУБЕ</h3>
        <h2 class="top-slider__title">Афтепати — это <i>Микс</i></h2>
        <p class="top-slider__desc">Мекка афтэпати в Москве</p>
      </div>
    </router-link>

  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style lang="scss">
.top-slider {

  .top-slider__slide {
    position: relative;
    display: flex;
    flex-flow: column nowrap;
    justify-content: end;
    align-content: end;

    &, & * {
      text-decoration: none;
    }

    &::before {
      content: '';
      display: block;
      position: absolute;
      top: 0;
      bottom: 0;
      right: 0;
      left: 0;;
      z-index: 2;
      background-color: rgba($color: #000000, $alpha: 0.33);
    }

    .top-slider__bg-img {
      position: absolute;
      top: 0;
      left: 0;
      bottom: 0;
      right: 0;
      z-index: 1;
    }

    .top-slider__text {
      position: relative;
      z-index: 3;

      .top-slider__subtitle {
        font-size: 1rem;
        letter-spacing: 0.7em;
        text-transform: uppercase;
        font-weight: 500;
        margin: 1rem 0;
      }

      .top-slider__title {
        font-size: 5rem;
        font-weight: 400;
        margin: 1rem 0;
      }

      .top-slider__desc {
        text-transform: uppercase;
        letter-spacing: 0.1em;
        margin: 1rem 0;
      }
    }
  }
}
</style>
