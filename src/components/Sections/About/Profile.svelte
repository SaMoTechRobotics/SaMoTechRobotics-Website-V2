<script lang="ts">
  export let name: string;

  let img: string = `images/photos/bios/${name}.webp`;
</script>

<div class="wrapper">
  <img src={img} alt="" />
  <div class="content">
    <h1>{name}</h1>
    <hr />
    <p>
      <slot />
    </p>
  </div>
</div>

<style lang="scss">
  .wrapper {
    padding: 1rem 1rem;

    display: grid;
    grid-template-columns: 13rem 1fr;
    grid-template-rows: 1fr;

    @media (max-width: 768px) {
        grid-template-columns: 1fr;
        grid-template-rows: 13rem 1fr;
    }

    img {
      width: 12rem;
      height: 12rem;
      border-radius: 50%;
      object-fit: cover;

      box-shadow: var(--img-shadow);
    }

    .content {
      padding: 1rem;

      font-family: var(--font);
      color: var(--text);

      h1 {
        font-size: 2rem;
        margin-top: -0.5rem;
        margin-bottom: 0;
      }

      hr {
        width: 4rem;
        margin: 0.5rem 0;
        color: var(--text);
      }

      p {
        font-size: 1rem;
        font-weight: normal;
        line-height: 2rem;
        color: var(--text);
      }


    }
  }
</style>
