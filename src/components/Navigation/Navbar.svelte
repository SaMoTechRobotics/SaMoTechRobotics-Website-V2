<script lang="ts">
  export let page: string;

  let menuOpen = false;

  let scrollY = 0;
</script>

<title>SaMoTech Robotics » {page.charAt(0).toUpperCase() + page.slice(1)}</title
>
<div class="navbar-wrapper" class:scrolled={scrollY > 30}>
  <div class="navbar-content">
    <div class="left-items">
      <a href="/"
        ><img src="/images/logos/samotech-logo.png" alt="" width="50" />
        <span>SaMoTech Robotics</span>
      </a>
    </div>
    <div class="right-items">
      <nav>
        <a href="/">
          <button class:active={page === "home"}>Home</button>
        </a>
        <a href="/about">
          <button class:active={page === "about"}>About</button>
        </a>
        <a href="/robot">
          <button class:active={page === "robot"}>Robot</button>
        </a>
        <a href="/donate">
          <button class:active={page === "donate"}>Donate</button>
        </a>
      </nav>
    </div>
    <div class="right-menu">
      <div class="menu" class:hidden={!menuOpen}>
        <div class="menu-items">
          <a href="/">
            <button class:active={page === "home"}>Home</button>
          </a>
          <a href="/about">
            <button class:active={page === "about"}>About</button>
          </a>
          <a href="/robot">
            <button class:active={page === "robot"}>Robot</button>
          </a>
          <a href="/donate">
            <button class:active={page === "donate"}>Donate</button>
          </a>
        </div>
      </div>
      <button
        class="hamburger"
        on:click={() => (menuOpen = !menuOpen)}
        class:open={menuOpen}
      >
        <span />
        <span />
        <span />
      </button>
    </div>
  </div>
</div>
<div class="padding" />

<svelte:window bind:scrollY />

<style lang="scss">
  .padding {
    height: 6rem;
  }

  .navbar-wrapper {
    z-index: 10;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    font-family: var(--font);
    transition: background-color 300ms ease-in-out, box-shadow 300ms ease-in-out;

    &.scrolled {
      background-color: rgba(0, 200, 255, 1);
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    }
  }

  .navbar-content {
    padding: 2rem 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: calc(100% - 2rem);
    transition: padding 300ms ease-in-out;

    .navbar-wrapper.scrolled & {
      padding: 0.5rem 2rem;
    }
  }

  .navbar-wrapper a {
    color: var(--text-inv);
    text-shadow: var(--text-shadow);
  }

  .left-items {
    font-size: 2rem;
    font-weight: bold;
    display: flex;
    align-items: top;
    justify-content: space-between;

    > a {
      display: flex;
      align-items: center;
      text-decoration: none;
      color: var(--text-inv);

      img {
        margin-right: 1rem;
        filter: brightness(0) invert(1) drop-shadow(var(--text-shadow));
      }

      span {
        @media (max-width: 712px) {
          display: none;
        }
      }
    }
  }

  .right-items {
    a:last-child {
      margin-right: 1rem;
    }

    a {
      text-decoration: none;

      button {
        font-weight: bold;
        font-size: 1.5rem;
        background-color: transparent;
        color: var(--text-inv);
        text-shadow: var(--text-shadow);
        cursor: pointer;

        padding: 0.5rem 1rem;
        border: none;
        border-radius: 1rem;

        transition: all 300ms ease-in-out;

        &.active {
          background-color: var(--bg);
          color: var(--primary);
          text-shadow: none;
          box-shadow: var(--text-shadow);
        }
      }
    }
  }

  .right-menu {
    button.hamburger {
      background-color: transparent;
      border: none;

      cursor: pointer;

      width: 2rem;
      height: 2rem;

      padding: 0.5rem 1rem;
      margin-right: 2rem;

      filter: drop-shadow(var(--text-shadow));

      span {
        background-color: var(--text-inv);

        display: block;
        width: 2rem;
        height: 0.25rem;
        border-radius: 1rem;

        position: absolute;
        left: 0;

        transition: transform 200ms ease-in-out, opacity 200ms ease-in-out,
          top 200ms ease-in-out;

        &:nth-child(1) {
          top: 0.3rem;
        }

        &:nth-child(2) {
          top: 0.9rem;
        }

        &:nth-child(3) {
          top: 1.5rem;
        }
      }

      &.open {
        span {
          background-color: var(--dark);

          &:nth-child(1) {
            top: 0.9rem;
            transform: rotate(180deg + 45deg);
          }

          &:nth-child(2) {
            opacity: 0;
          }

          &:nth-child(3) {
            top: 0.9rem;
            transform: rotate(180deg - 45deg);
          }
        }
      }
    }

    .menu {
      position: absolute;
      top: 2rem;
      right: 1.5rem;

      padding: 1rem 1rem;
      padding-top: 3rem;

      background-color: var(--bg);
      border-radius: 1rem;

      transform-origin: top right;
      opacity: 1;
      transform: scale(1);

      transition: opacity 300ms ease-in-out, transform 300ms ease-in-out;

      .menu-items {
        display: flex;
        flex-direction: column;
        align-items: center;

        a {
          text-decoration: none;

          button {
            font-weight: bold;
            font-size: 1.5rem;
            background-color: transparent;
            color: var(--dark);
            cursor: pointer;

            // background-color: var(--text);

            padding: 0.5rem 1rem;
            border: none;
            border-radius: 1rem;

            transition: background-color 300ms ease-in-out;
          }
        }
      }

      &.hidden {
        opacity: 1;
        transform: scale(0.25);
      }
    }
  }

  @media (min-width: 550px) {
    .right-menu {
      display: none;
    }
  }

  @media (max-width: 550px) {
    .right-items {
      display: none;
    }

    .right-menu {
      display: block;
    }
  }
</style>
