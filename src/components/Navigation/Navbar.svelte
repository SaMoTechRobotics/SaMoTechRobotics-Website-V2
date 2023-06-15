<script lang="ts">
  export let page: string;

  let scrollY = 0;
</script>

<title>SaMoTech Robotics » {page.charAt(0).toUpperCase() + page.slice(1)}</title
>
<div class="navbar-wrapper" class:scrolled={scrollY > 50}>
  <div class="navbar-content">
    <div class="left-items">
      <a href="/"
        ><img src="/images/logos/samotech-logo.png" alt="" width="50" />
        <span>SaMoTech Robotics</span>
      </a>
    </div>
    <div class="right-items">
      <nav>
        <a href="/" class:active={page === "home"}>Home</a>
        <a href="/about" class:active={page === "about"}>About</a>
        <a href="/donate" class:active={page === "donate"}>Donate</a>
      </nav>
    </div>
    <div class="right-hamburger">
      <button class="" />
    </div>
  </div>
</div>
<div class="padding" />

<svelte:window bind:scrollY />

<style>
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
  }

  .navbar-wrapper.scrolled {
    /* background-color: var(--bg); */
    background-color: rgba(0, 200, 255, 1);
    /* backdrop-filter: blur(5px); */
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  }

  .navbar-content {
    padding: 2rem 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: calc(100% - 2rem);
    transition: padding 300ms ease-in-out;
  }

  .navbar-wrapper.scrolled > .navbar-content {
    padding: 0.5rem 2rem;
  }

  .navbar-wrapper a {
    color: var(--text-inv);
    transition: color 300ms ease-in-out;

    text-shadow: var(--text-shadow);
  }
  .navbar-wrapper.scrolled a {
    /* color: var(--primary); */
    /* text-shadow: none; */
  }

  .left-items {
    font-size: 2rem;
    font-weight: bold;

    display: flex;
    align-items: top;
    justify-content: space-between;
  }

  .right-items {
    font-size: 1.2rem;
  }

  .left-items > a {
    display: flex;
    align-items: center;
    text-decoration: none;

    color: var(--text-inv);
  }

  .left-items > a img {
    margin-right: 1rem;

    filter: brightness(0) invert(1) drop-shadow(var(--text-shadow));
  }

  .scrolled .left-items > a img {
    /* filter: none; */
  }

  @media (max-width: 712px) {
    .left-items > a span {
      display: none;
    }
  }

  .right-items a:last-child {
    margin-right: 1rem;
  }

  @media (min-width: 300px) {
    .right-hamburger {
      display: none;
    }
  }

  @media (max-width: 300px) {
    .right-items {
      display: none;
    }
    .right-hamburger {
      display: block;
    }
  }

  .right-items a {
    color: var(--text-inv);
    text-decoration: none;
    padding: 0.5rem 1rem;

    border-radius: 1rem;
    border: 2px solid transparent;

    transition: border-color 200ms ease-in-out, border-radius 200ms ease-in-out;
  }

  .right-items a.active {
    border-radius: 2rem;
    border: 2px solid var(--text-inv);
  }

  /*.scrolled .right-items a.active {
  border: 2px solid var(--text-inv);
  }*/
</style>
