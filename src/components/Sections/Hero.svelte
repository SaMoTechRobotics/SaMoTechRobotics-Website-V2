<script lang="ts">
  export let img: string;
</script>

<div class="wrapper">
  <img src={img} alt="" />
</div>

<style lang="scss">
  .wrapper {
    padding: 2rem 2rem;
    padding-bottom: 0;

    display: flex;
    justify-content: center;
    align-items: center;

    @media (max-width: 800px) {
      padding: 0rem 0.1rem;
      padding-top: 2rem;
    }

    img {
      max-width: 100%;
      max-height: calc(100vh - 6rem - 5rem);

      object-fit: contain;
      border-radius: 1rem;

      box-shadow: var(--img-shadow);
    }
  }
</style>
