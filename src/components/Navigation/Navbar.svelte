<script lang="ts">
  export let page: string;
</script>

<title>SaMoTech Robotics » {page.charAt(0).toUpperCase() + page.slice(1)}</title
>
<div class="navbar-wrapper">
  <div class="left-items">
    <a href="/">Home</a>
  </div>
  <div class="right-items">
    <nav>
      <a href="/" class:active={page === "home"}>Home</a>
      <a href="/about" class:active={page === "about"}>About</a>
      <a href="/donate" class:active={page === "donate"}>Donate</a>
    </nav>
  </div>
</div>

<style>
  .navbar-wrapper {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem;
    background: var(--primary);
  }

  .left-items {
    font-size: 2rem;
    font-weight: bold;
  }

  .right-items {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  a {
    color: var(--text);
    text-decoration: none;
  }

  a.active {
    border-bottom: 2px solid var(--text);
  }
</style>
