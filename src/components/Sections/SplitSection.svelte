<script lang="ts">
  export let title: string;
  export let img: string;
  export let textSide: "left" | "right" = "right";
  export let noBackground: "true" | "false" = "false";
</script>

<div
  class="content"
  class:right={textSide === "right"}
  class:noBackground={noBackground === "true"}
>
  <div class="card">
    <h1>{title}</h1>
    <p>
      <slot />
    </p>
    <div class="buttons">
      <slot name="buttons" />
    </div>
  </div>
  <img src={img} alt="" />
</div>

<style lang="scss">
  .content {
    background-color: var(--bg);
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr;
    gap: 0px 0px;
    height: 100%;

    font-family: var(--font);
    color: var(--text);

    padding: 2rem 2rem;

    //&.noBackground {
    //  background-color: transparent;
    //  color: var(--text-inv);
    //  text-shadow: var(--text-shadow);
    //}

    &.noBackground {
      margin: 2rem;
      margin-top: 0;
      padding: 1rem;
      border-radius: 15px;
    }

    &.right {
      grid-template-columns: 1fr 1fr;

      > .card {
        order: 2;
      }

      > img {
        order: 1;
      }
    }

    @media (max-width: 980px) {
      grid-template-columns: 1fr;
      grid-template-rows: 1fr;
      &.right {
        grid-template-columns: 1fr;
      }

      > .card {
        order: 2;
      }

      > img {
        order: 1;
      }
    }

    .card {
      padding: 2rem;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      h1 {
        font-size: 2rem;
        text-align: center;
        margin-bottom: 0;
      }

      p {
        color: var(--text-gray);
        font-size: 1rem;
        text-align: center;
        line-height: 2rem;
      }

      .buttons {
        margin-top: 1rem;

        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;

        text-align: center;
      }
    }

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 1rem;

      box-shadow: var(--img-shadow);
    }
  }
</style>
