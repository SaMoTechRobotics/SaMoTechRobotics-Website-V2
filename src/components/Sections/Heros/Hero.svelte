<script lang="ts">
    import {onMount} from "svelte";

    export let img: string;

    let y = 0;

    onMount(() => {
        if (window.innerWidth < 880) {
            y = -300;
        }
        window.addEventListener('scroll', () => {
            if (window.innerWidth < 880) {
                y = -300;
                return;
            }
            y = window.scrollY;
        });
    });
</script>

<div class="wrapper" style="background-image: url({img}); background-position-y: {-y / 3 + 20}px;">
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

    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    background-attachment: fixed;

    @media (max-width: 880px) {
      background-size: contain;
      background-position-y: 100px;

      height: calc(100vh - 100px);
    }

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

      @media (max-width: 880px) {
        padding-bottom: 0;
        height: calc(100% - 100px);
      }
    }


  }
</style>
