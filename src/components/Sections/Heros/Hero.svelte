<script lang="ts">
    import {onMount} from "svelte";

    export let img: string;

    let y = 0;

    onMount(() => {
        window.addEventListener('scroll', () => {
            y = window.scrollY;
        });
    });
</script>

<div class="wrapper" style="background-image: url({img}); background-position-y: {-y / 3}px;">
    <!--    <img src={img} alt=""/>-->
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

    margin-bottom: -0.5rem;

    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    background-attachment: fixed;

    img {
      width: 100%;
      height: 100%;


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
