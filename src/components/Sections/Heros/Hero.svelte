<script lang="ts">
    export let img: string;
</script>

<div class="wrapper">
    <img src={img} alt=""/>
    <div class="overlay">
        <slot/>
    </div>
</div>

<style lang="scss">
  .wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100vw;
    height: 100vh;

    img {
      width: 100%;
      height: 100%;

      margin-bottom: -10px;

      object-fit: cover;
    }

    .overlay {
      position: absolute;
      width: 100%;
      height: 100%;

      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: end;
      padding-bottom: 6rem;
    }


  }
</style>
