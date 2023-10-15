<div class="wrapper">
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"
    ><path
      fill="var(--bg)"
      fill-opacity="1"
      d="M0,224L120,213.3C240,203,480,181,720,165.3C960,149,1200,139,1320,133.3L1440,128L1440,320L1320,320C1200,320,960,320,720,320C480,320,240,320,120,320L0,320Z"
    /></svg
  >
  <div class="content">
    <slot />
  </div>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    viewBox="0 0 1440 320"
    style="transform: rotate(180deg);"
    ><path
      fill="var(--bg)"
      fill-opacity="1"
      d="M0,224L120,213.3C240,203,480,181,720,165.3C960,149,1200,139,1320,133.3L1440,128L1440,320L1320,320C1200,320,960,320,720,320C480,320,240,320,120,320L0,320Z"
    /></svg
  >
</div>

<style lang="scss">
  .wrapper {
    svg {
      z-index: -1;
      margin: 0;
      margin-bottom: -30px;
      filter: drop-shadow(0px 0px 20px rgba(0, 0, 0, 0.25));
      clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
    }

    .content {
      z-index: 1;
      background-color: var(--bg);
      outline: 5px solid var(--bg);
    }
  }
</style>
