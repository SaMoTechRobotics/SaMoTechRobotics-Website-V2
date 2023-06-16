<script>
</script>

<div class="wrapper">
  <div class="background" />
  <div class="bar">
    <slot />
  </div>
</div>

<style lang="scss">
  .wrapper {
    position: relative;
    padding-top: 7rem;
    // height: 5rem;

    display: flex;
    align-items: center;
    justify-content: center;

    .bar {
      z-index: 1;
      background-color: var(--bg);
      padding: 2rem 4rem;
      border-radius: 1rem;
      box-shadow: var(--box-shadow);

      height: 100%;

      display: grid;
      grid-template-columns: repeat(4, 1fr);
      grid-template-rows: 1fr;

      overflow: hidden;

      gap: 2rem;

      transform: translateY(-15%);

      @media (max-width: 880px) {
        gap: 0rem;
      }

      @media (max-width: 800px) {
        padding: 2rem 0rem;
      }

      @media (max-width: 650px) {
        grid-template-columns: repeat(2, 1fr);
        grid-template-rows: repeat(2, 1fr);

        row-gap: 2rem;
      }
    }

    .background {
      background-color: var(--bg);
      position: absolute;
      top: 70%;
      left: 0;
      width: 100%;
      height: 30%;
    }
  }
</style>
