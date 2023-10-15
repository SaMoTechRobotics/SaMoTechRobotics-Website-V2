<script lang="ts">
    export let title: string;
    export let img: string = "";
    export let imgs: string = "";
    export let textSide: "left" | "right" = "right";
    export let noBackground: "true" | "false" = "false";

    let imgsArray: string[] = [];
    $: {
        if (imgs) {
            imgsArray = imgs.split(",");
        }
    }
</script>

<div
        class="content"
        class:right={textSide === "right"}
        class:noBackground={noBackground === "true"}
>
    <div class="card">
        <h1>{title}</h1>
        <p>
            <slot/>
        </p>
        <div class="buttons">
            <slot name="buttons"/>
        </div>
    </div>
    {#if imgsArray.length > 0}
        <div class="imgs">
            {#each imgsArray as img}
                <img src={img} alt=""/>
            {/each}
        </div>
    {/if}
    {#if img !== ""}
        <div class="img">
            <img src={img} alt=""/>
        </div>
    {/if}
    <slot name="bottom"/>
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

      @media (max-width: 700px) {
        margin: 1rem;
        margin-top: 0;
        padding: 1rem;
        border-radius: 15px;
      }
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
      justify-content: start;
      align-items: center;

      h1 {
        font-size: 2rem;
        text-align: center;
        margin-bottom: 0;
      }

      p {
        color: var(--text-gray);
        font-size: 1rem;
        text-align: left;
        line-height: 2rem;
      }

      .buttons {
        margin-top: -1rem;

        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;

        text-align: center;
      }
    }

    .imgs {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      img {
        margin-bottom: 1rem;
      }
    }

    .img {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      margin-bottom: 2rem;
    }

    img {
      max-width: 100%;
      object-fit: contain;
      border-radius: 1rem;

      box-shadow: var(--img-shadow);
    }
  }
</style>
