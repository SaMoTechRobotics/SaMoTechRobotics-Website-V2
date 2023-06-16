<script>
  import Background from "../components/Sections/Background.svelte";
</script>

<Background />
<div class="wrapper">
  <h1>404</h1>
  <p>There is no page here</p>
  <p>Return to <a href="/">Home</a></p>
</div>

<style lang="scss">
  .wrapper {
    font-family: var(--font);
    color: var(--text-inv);
    text-shadow: var(--text-shadow);

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-size: 2rem;

    h1 {
      margin-top: 10rem;
      font-size: 5rem;
      margin-bottom: 0;
    }

    p {
      font-size: 2rem;
    }

    a {
      color: var(--dark);
      text-decoration: none;
      text-shadow: none;

      &:hover {
        text-decoration: underline;
      }
    }
  }
</style>
