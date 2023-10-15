<script>
  import Sponsor from "./Sponsor.svelte";
</script>

<div class="wrapper">
  <div class="content">
    <h1>Our Sponsors</h1>
    <p>
      We would like to thank the main sponsor of our rookie year, ZipRecruiter, along with supporting sponsors, Rowe Neurology Institute and Panasonic for their generous support. Your contributions made SaMoTech possible and have allowed us to pursue our interests in robotics and engineering. We greatly appreciate your belief in us and the opportunities you have provided.
    </p>
  </div>
  <Sponsor to="https://www.ziprecruiter.com/" sponsor="ZipRecruiter" />
  <div class="sponsors">
    <Sponsor to="https://www.na.panasonic.com/" sponsor="Panasonic" />
    <Sponsor to="https://www.neurokc.com/" sponsor="RNI" />
<!--    <Sponsor to="https://www.gobilda.com/" sponsor="goBilda" />-->
    <div />
  </div>
</div>

<style lang="scss">
  .wrapper {
    padding: 2rem 2rem;
    padding-bottom: 0;

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
        font-size: 1.2rem;
        line-height: 2rem;
        //max-width: 50rem;
      }
    }

    .sponsors {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      //grid-template-rows: repeat(2, 1fr);
      grid-gap: 2rem;

      padding: 2rem 0rem;

      @media (max-width: 800px) {
        grid-template-columns: repeat(1, 1fr);
        grid-template-rows: repeat(4, 1fr);
      }
    }
  }
</style>
