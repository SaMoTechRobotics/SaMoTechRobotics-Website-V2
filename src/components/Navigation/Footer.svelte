<script>
    import SocialButton from "../Interactive/SocialButton.svelte";
    import {page} from "$app/stores";
</script>

<div class="wrapper" class:noWaves={$page.url.pathname !== "/"}>
    <svg class="waves" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
         viewBox="0 20 150 28" preserveAspectRatio="none" shape-rendering="auto">
        <defs>
            <path id="gentle-wave" d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z"/>
        </defs>
        <g class="parallax">
            <use xlink:href="#gentle-wave" x="48" y="0" fill="rgba(0, 200, 255, 0.4)"/>
            <use xlink:href="#gentle-wave" x="48" y="3" fill="rgba(0, 200, 255, 0.6)"/>
            <use xlink:href="#gentle-wave" x="48" y="5" fill="rgba(0, 200, 255, 0.8)"/>
            <use xlink:href="#gentle-wave" x="48" y="7" fill="rgba(0, 200, 255, 1)"/>
        </g>
    </svg>
    <div class="content">
        <div class="social">
            <SocialButton icon="akar-icons:instagram-fill" white={$page.url.pathname !== "/"}
                          to="https://www.instagram.com/samotechrobotics/"/>
            <SocialButton icon="akar-icons:github-fill" white={$page.url.pathname !== "/"}
                          to="https://github.com/SaMoTechRobotics"/>
            <SocialButton icon="akar-icons:youtube-fill" white={$page.url.pathname !== "/"}
                          to="https://www.youtube.com/@samotechrobotics"/>
        </div>
        <p>Contact us at <a href="mailto:samotechrobotics@gmail.com">samotechrobotics@gmail.com</a></p>
    </div>
</div>

<style lang="scss">
  .wrapper {
    background-color: var(--bg);
    color: var(--text-inv);

    height: 10rem;
    width: 100vw;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    &.noWaves {
      height: 8rem;

      .waves {
        display: none;
      }

      .content {
        background-color: var(--bg);

        p {
          color: var(--text);

          a {
            color: var(--text);
          }
        }
      }
    }

    .content {
      background-color: var(--primary);
      width: 100%;
      height: 100%;
      padding-top: 1rem;

      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      .social {

        display: flex;
        align-items: center;
        justify-content: center;

        :global(> a) {
          margin: 0 0.5rem;
        }
      }

      p {
        font-family: var(--font);
        margin: 0;
        padding: 0.5rem;

        a {
          color: var(--text-inv);
          text-decoration: none;
          transition: all 0.2s ease-in-out;

          &:hover {
            text-decoration: underline;
          }
        }
      }

    }

    .waves {
      width: 100%;
    }

    .parallax {
      > use {
        animation: move-forever 25s cubic-bezier(.55, .5, .45, .5) infinite;


        @keyframes move-forever {
          0% {
            transform: translate3d(-90px, 0, 0);
          }
          100% {
            transform: translate3d(85px, 0, 0);
          }
        }

        @media (max-width: 480px) {
          .waves {
            display: none;
          }
        }

        &:nth-child(1) {
          animation-delay: -2s;
          animation-duration: 7s;
        }

        &:nth-child(2) {
          animation-delay: -3s;
          animation-duration: 10s;
        }

        &:nth-child(3) {
          animation-delay: -4s;
          animation-duration: 13s;
        }

        &:nth-child(4) {
          animation-delay: -5s;
          animation-duration: 20s;
        }
      }
    }
  }

</style>
