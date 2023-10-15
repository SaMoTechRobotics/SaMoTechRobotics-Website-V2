<div class="background" />

<style lang="scss">
  .background {
    background: linear-gradient(
      45deg,
      var(--dark) 0%,
      var(--primary) 50%,
      rgb(63, 207, 255) 75%,
      rgb(53, 242, 255) 100%
    );
    background-size: 200% 200%;
    background-attachment: fixed;
    position: fixed;
    top: 0;
    left: 0;
    z-index: -1;
    width: 100vw;
    height: 100vh;

    animation: bg-gradient 10s ease-in-out infinite;
  }

  @keyframes bg-gradient {
    0% {
      background-position: 100% 50%;
    }
    50% {
      background-position: 0% 50%;
    }
    100% {
      background-position: 100% 50%;
    }
  }
</style>
