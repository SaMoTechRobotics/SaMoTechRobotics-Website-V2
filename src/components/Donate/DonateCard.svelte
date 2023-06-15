<script lang="ts">
  import Icon from "@iconify/svelte";

  export let type: "donate" | "sponsor";
  export let title: string;
  export let to: string = "";

  export let tier: "1" | "2" | "3" = "1";
</script>

{#if type === "donate"}
  <a href={to} target="_blank">
    <div class="card donate">
      <div class="icon">
        <slot name="icon" />
      </div>
      <h1>{title}</h1>
      <p><slot /></p>
      <button>Donate</button>
    </div>
  </a>
{:else}
  <div class="card sponsor">
    <div class="icon">
      <Icon
        icon="fa6-solid:medal"
        color={tier === "1" ? "#ffd700" : tier === "2" ? "#c0c0c0" : "#cd7f32"}
        height="60"
      />
    </div>
    <h1><span>$</span>{title}</h1>
    <p>
      <slot />
    </p>
  </div>
{/if}

<style lang="scss">
  a {
    text-decoration: none;
  }

  .card {
    background-color: var(--bg);
    font-family: var(--font);
    color: var(--text);
    border-radius: 1rem;
    padding: 5rem 1rem;
    padding-bottom: 3rem;

    display: flex;
    flex-direction: column;
    align-items: center;

    min-width: 15rem;
    max-width: 15rem;
    @media (max-width: 768px) {
      min-width: 10rem;
    }
    @media (max-width: 450px) {
      min-width: 2rem;
    }

    box-shadow: var(--box-shadow);
    transition: box-shadow 200ms ease-in-out, margin-top 200ms ease-in-out,
      outline 100ms ease-in-out;

    &.donate:hover {
      box-shadow: var(--box-shadow-hover);
      margin-top: -0.2rem;
    }

    &.sponsor:hover {
      outline: 5px solid var(--dark);
    }

    .icon {
      transition: transform 200ms ease-in-out;

      &:hover {
        transform: scale(1.05);
      }
    }

    h1 {
      font-size: 2rem;
      font-weight: bold;
      margin-bottom: 0;

      span {
        font-family: sans-serif;
        font-size: 2rem;
        margin-right: 0.5rem;
      }

      @media (max-width: 450px) {
        font-size: 1.5rem;
      }
    }

    &.donate p {
      color: var(--text-muted);
      font-size: 1.2rem;
      text-align: center;
      height: 7.2rem;
    }

    button {
      // background-color: var(--dark);
      background-color: transparent;
      color: var(--dark);
      font-size: 1.2rem;
      font-weight: bold;
      border: 3px outset var(--primary);
      cursor: pointer;

      padding: 1rem 2rem;
      margin-top: 1rem;

      border-radius: 1rem;
      box-shadow: var(--box-shadow);
      // text-shadow: var(--text-shadow);

      transition: box-shadow 200ms ease-in-out;

      &:hover {
        box-shadow: var(--box-shadow-hover);
      }
    }
  }
</style>
