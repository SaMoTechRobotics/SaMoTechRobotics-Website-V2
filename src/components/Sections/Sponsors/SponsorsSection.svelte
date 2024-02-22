<script>
    import Sponsor from "./Sponsor.svelte";
</script>

<div class="wrapper">
    <div class="content">
        <h1>Our Sponsors</h1>
        <p>
            We would like to thank our main sponsors of our 2023-2024 season, ZipRecruiter, Boeing, and Rotary Club of
            Santa Monica
            along with supporting sponsors, Yahoo, Panasonic, and Czeh for their generous support. Your contributions
            made SaMoTech possible and have allowed us to pursue our interests in robotics and engineering. We greatly
            appreciate your belief
            in us and the opportunities you have provided.
        </p>
    </div>
    <div style="transform: scale(0.75)">
        <Sponsor to="https://www.ziprecruiter.com/" sponsor="ZipRecruiter"/>
    </div>
    <div class="sponsors">
        <Sponsor to="" sponsor="Boeing"/>
        <div style="transform: scale(0.5)">
            <Sponsor to="" sponsor="RotaryClub-GEAR"/>
        </div>
    </div>
    <div class="sponsors">
        <Sponsor to="" sponsor="Yahoo"/>
        <Sponsor to="https://www.na.panasonic.com/" sponsor="Panasonic"/>
        <div style="transform: scale(0.5)">
            <Sponsor to="" sponsor="Czeh"/>
        </div>
        <div/>
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
        font-size: 1.2rem;
        line-height: 2rem;
        //max-width: 50rem;
      }
    }

    .sponsors {
      width: 100%;
      height: 100%;

      display: inline-grid;

      grid-template-columns: repeat(auto-fit, minmax(400px, 1.5fr));

      //align content to the center
      justify-content: center;
      align-items: center;
      grid-auto-rows: 1fr;

      grid-gap: 2rem;

      padding: 0 2rem 2rem;
      margin-top: -2rem;

      @media (max-width: 800px) {
        grid-template-columns: repeat(1, 1fr);
        grid-template-rows: repeat(auto-fit, 1fr);
      }
    }
  }
</style>
