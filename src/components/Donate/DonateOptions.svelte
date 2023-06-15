<script lang="ts">
  let active: "donate" | "sponsor" = "donate";
</script>

<div class="wrapper">
  <div class="toggle">
    <button
      class:active={active === "donate"}
      on:click={() => (active = "donate")}>Donate</button
    >
    <button
      class:active={active === "sponsor"}
      on:click={() => (active = "sponsor")}>Sponsor</button
    >
    <div class="toggle-bg" class:move={active === "sponsor"} />
  </div>
  <div class="options">
    <div class="cards" class:hidden={active !== "donate"}>
      <slot name="donate" />
    </div>
    <div class="cards" class:hidden={active !== "sponsor"}>
      <slot name="sponsor" />
    </div>
  </div>
</div>
{#if active === "sponsor"}
  <div class="button-wrapper">
    <a href="mailto:samotechrobotics.com?subject=Sponsoring SaMoTech Robotics">
      <button>Contact Us</button>
    </a>
  </div>
{/if}

<style lang="scss">
  .wrapper {
    border-radius: 1rem;

    display: flex;
    flex-direction: column;
    align-items: center;

    .toggle {
      background-color: var(--bg);
      border-radius: 2rem;

      position: relative;
      display: flex;
      justify-content: center;
      margin: 1rem 0;

      max-width: 15rem;

      box-shadow: var(--box-shadow);

      button {
        z-index: 1;
        background-color: transparent;
        color: var(--dark);
        font-size: 1rem;
        font-weight: bold;
        border: none;
        cursor: pointer;

        padding: 0.5rem 1rem;

        width: 100%;
        height: 100%;

        transition: color 200ms ease-in-out, text-shadow 200ms ease-in-out;
      }

      button.active {
        color: var(--text-inv);
        text-shadow: var(--text-shadow);
      }

      .toggle-bg {
        z-index: 0;
        background-color: var(--dark);
        border-radius: 1rem;

        position: absolute;
        top: 0;
        left: 0;
        width: 50%;
        height: 100%;
        transition: left 200ms ease-in-out;
      }

      .toggle-bg.move {
        left: 50%;
      }
    }

    .options {
      display: flex;
      justify-content: center;

      :global(.cards > div) {
        display: grid;
        grid-auto-flow: column;
        grid-template-columns: repeat(1fr);
        grid-template-rows: 1fr;
        gap: 1rem;
      }

      > .cards.hidden {
        display: none;
      }
    }
  }

  .button-wrapper {
    padding: 1rem;

    display: flex;
    justify-content: center;

    button {
      background-color: var(--dark);
      color: var(--text-inv);
      font-size: 1.5rem;
      font-weight: bold;
      border: none;
      cursor: pointer;

      border-radius: 1rem;

      text-shadow: var(--text-shadow);
      box-shadow: var(--box-shadow);

      padding: 0.5rem 1rem;

      width: 12rem;
      height: 100%;

      transition: background-color 200ms ease-in-out,
        box-shadow 200ms ease-in-out;

      &:hover {
        background-color: rgba(0, 0, 0, 0.1);
        box-shadow: var(--box-shadow-hover);
      }

      a {
        color: var(--text-inv);
        text-decoration: none;
      }
    }
  }
</style>
