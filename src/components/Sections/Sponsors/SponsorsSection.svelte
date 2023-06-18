<script>
  import Sponsor from "./Sponsor.svelte";
</script>

<div class="wrapper">
  <div class="content">
    <h1>Our Sponsors</h1>
    <p>
      We are grateful for the support of our sponsors. Without them, we wouldn't
      be able to accomplish what we do.
    </p>
  </div>
  <div class="sponsors">
    <Sponsor to="https://www.ziprecruiter.com/" sponsor="ZipRecruiter" />
    <Sponsor to="https://www.na.panasonic.com/" sponsor="Panasonic" />
    <Sponsor to="https://www.gobilda.com/" sponsor="goBilda" />
    <Sponsor to="https://www.neurokc.com/" sponsor="RNI" />
    <div />
  </div>
</div>

<style lang="scss">
  .wrapper {
    padding: 2rem 2rem;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    font-family: var(--font);

    .content {
      text-align: center;
      margin-bottom: 2rem;

      color: var(--text-inv);
      text-shadow: var(--text-shadow);

      h1 {
        font-size: 3rem;
      }

      p {
        font-size: 1.5rem;
        max-width: 50rem;
      }
    }

    .sponsors {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      grid-template-rows: repeat(2, 1fr);
      grid-gap: 2rem;

      @media (max-width: 800px) {
        grid-template-columns: repeat(1, 1fr);
        grid-template-rows: repeat(4, 1fr);
      }
    }
  }
</style>
