<script lang="ts">
  export let img: string;
</script>

<img src={img} alt="" />

<style lang="scss">
    img {
      width: 100vw;
      height: 100vh;

      margin-bottom: -10px;

      object-fit: cover;
    }
</style>
