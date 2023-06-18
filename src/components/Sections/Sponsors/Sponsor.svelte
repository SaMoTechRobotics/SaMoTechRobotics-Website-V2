<script lang="ts">
  export let to: string;
  export let sponsor: string;
</script>

<a href={to} target="_blank">
  <div class="wrapper">
    <img src={`images/logos/sponsors/${sponsor}.webp`} alt="" />
  </div>
</a>

<style lang="scss">
  .wrapper {
    width: 100%;
    height: 100%;

    display: flex;
    justify-content: center;
    align-items: center;

    img {
      max-width: 75%;
      max-height: 100%;

      transition: transform 200ms ease-in-out;

      &:hover {
        transform: scale(1.05);
      }
    }
  }
</style>
