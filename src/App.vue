<template>
  <div class="mix-layout bg-dark t-white">

    <aside class="mix-layout__sidebar mix-layout__sidebar_left sticky-top">
      <div class="mix-layout__top-btn">
        <button class="btn_text top-btn t-white w-100">Меню</button>
      </div>
      <span class="mix-layout__number t-center">01</span>
      <footer class="sidebar__footer pb-3">
        <button class="btn_text t-white">
          <span class="t-muted t-vertical_reverse">Сейчас в клубе</span>
          <span class="icon">
            <img src="/assets/img/icons/play.svg" class="img-contain" alt="">
          </span>
        </button>
      </footer>
    </aside>

    <main class="mix-layout__content">

      <header class="mix-layout__header t-center p-3">
        <router-link to="/" class="t-white logo" title="На главную">
          <img src="/assets/img/logo/01 1@3x.png" class="img-contain" alt="Микс">
        </router-link>
      </header>

      <section class="t-center rounded-xl">
        <img src="/assets/img/top-slider/SfyXGMjOp0c 1.png" class="img-fluid" alt="">
      </section>

      <router-view/>

      <footer class="small t-center py-2">МИКС Afterparty © 2023 All Rights Reserved</footer>

    </main>

    <aside class="mix-layout__sidebar mix-layout__sidebar_right sticky-top">
      <div class="mix-layout__top-btn">
        <button class="btn_text t-white w-100">Контакты</button>
      </div>
      <span class="mix-layout__number t-center">05</span>
      <footer class="sidebar__footer pb-3">
        <button class="btn_text t-vertical t-white">Женская клубная карта</button>
      </footer>
    </aside>
  </div>

</template>

<style lang="scss">
@import '@/assets/styles/tokens';

.mix-layout {
  display: grid;
  grid-template-columns: 194px 1fr 194px;

  .mix-layout__sidebar {
    width: 194px;
    height: 100vh;
    overflow-y: auto;

    display: grid;
    grid-template-rows: minmax(min-content, 1fr) minmax(max-content, 1fr) minmax(max-content, 1fr);

    .mix-layout__number {
      display: flex;
      justify-content: center;
      align-content: center;
      justify-items: center;
      align-items: center;
    }

    .mix-layout__top-btn {
      display: grid;
      grid-template-rows: minmax(1f, 1fr);

      button {
        height: 194px;
        max-height: 100%;
      }
    }

    .sidebar__footer {
      display: flex;
      justify-content: center;
      align-items: end;

      .btn_text {
        display: flex;
        flex-flow: column nowrap;
        align-items: center;
        gap: 2rem;

        .icon {
          font-size: 2rem;
          width: 1em;
          height: 1em;
        }
      }
    }
  }

  .mix-layout__header {
    min-height: 194px;
    display: flex;
    align-items: center;
    justify-content: center;

    .logo {
      height: 72px;
      width: 121px;
    }
  }

  .mix-layout__content {}
}
</style>
