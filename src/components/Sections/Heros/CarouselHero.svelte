<script lang="ts">
  export let imgs: string;

  let index = 0;
</script>

<div class="wrapper">
  <div class="images">
    {#each imgs.split(",") as img, i}
      <img src={img} alt="" id={`${i}`} class:hidden={i !== index} />
    {/each}
  </div>
  <div class="selectors">
    {#each imgs.split(",") as img, i}
      <div
        class="selector"
        class:selected={i === index}
        on:click={() => (index = i)}
        on:keypress={() => (index = i)}
      />
    {/each}
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

    @media (max-width: 800px) {
      padding: 0rem 0.1rem;
      padding-top: 2rem;
    }

    .images {
      img {
        max-width: 100%;
        max-height: calc(100vh - 6rem - 5rem);

        object-fit: contain;
        border-radius: 1rem;

        box-shadow: var(--img-shadow);

        &.hidden {
          display: none;
        }
      }
    }

    .selectors {
      display: flex;
      justify-content: center;
      align-items: center;

      .selector {
        background-color: red;
        padding: 1rem;
        margin: 1rem;
        width: 1rem;
        height: 1rem;
      }
    }
  }
</style>
