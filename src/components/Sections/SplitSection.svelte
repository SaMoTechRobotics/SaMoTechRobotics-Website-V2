<script lang="ts">
  export let title: string;
  export let img: string;
  export let textSide: "left" | "right" = "right";
</script>

<div class="content" class:right={textSide === "right"}>
  <div class="card">
    <h1>{title}</h1>
    <p>
      <slot />
    </p>
    <slot class="buttons" name="buttons" />
  </div>
  <img src={img} alt="" />
</div>

<style lang="scss">
  .content {
    display: grid;
    grid-template-columns: 1fr 1.5fr;
    grid-template-rows: 1fr;
    gap: 0px 0px;
    height: 100%;

    font-family: var(--font);

    padding: 4rem 2rem;
    padding-bottom: 0;

    &.right {
      grid-template-columns: 1.5fr 1fr;

      > .card {
        order: 2;
      }

      > img {
        order: 1;
      }
    }

    @media (max-width: 980px) {
      grid-template-columns: 1fr;
      grid-template-rows: 1fr 1fr;

      > .card {
        order: 1;
      }

      > img {
        order: -1;
      }
    }

    @media (max-width: 550px) {
      grid-template-rows: 1fr 0.4fr;
    }

    .card {
      padding: 2rem;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      color: var(--text-inv);
      text-shadow: var(--text-shadow);

      h1 {
        font-size: 2rem;
        text-align: center;
        margin-bottom: 0;
      }

      p {
        font-size: 1rem;
        text-align: center;
      }

      > .buttons {
        margin-top: 1rem;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
      }
    }

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 1rem;

      box-shadow: var(--box-shadow);
    }
  }
</style>
