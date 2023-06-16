<script>
  import SocialButton from "../Interactive/SocialButton.svelte";
</script>

<div class="wrapper">
  <div class="social">
    <SocialButton to="" icon="akar-icons:instagram-fill" />
    <SocialButton to="" icon="akar-icons:github-fill" />
    <SocialButton to="" icon="akar-icons:youtube-fill" />
  </div>
</div>

<style lang="scss">
  .wrapper {
    background-color: var(--bg);
    color: var(--text-inv);

    padding: 2rem 2rem;
    height: 5rem;
    width: calc(100% - 4rem);

    display: flex;
    justify-content: center;
    align-items: center;
  }

  .social {
    display: flex;
    align-items: center;
    justify-content: space-between;

    :global(> a) {
      margin: 0 0.5rem;
    }
  }
</style>
