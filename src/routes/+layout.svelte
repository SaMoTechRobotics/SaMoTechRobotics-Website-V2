<script>
  import { page } from "$app/stores";
  import Navbar from "../components/Navigation/Navbar.svelte";
</script>

<Navbar page={$page.url.pathname.replace("/", "") || "home"} />

<slot />

<style>
  @import url("https://fonts.googleapis.com/css2?family=Secular+One&display=swap");

  :root {
    --bg: rgb(239, 253, 255);
    --bg-secondary: #f5f5f5;

    --primary: rgba(0, 200, 255, 1);
    --dark: rgba(2, 145, 184, 1);
    --secondary: rgba(154, 218, 244, 1);

    --text: #434343;
    --text-inv: #fff;
    --text-muted: #626262;

    --text-shadow: 0 2px 2px rgba(0, 0, 0, 0.3);
    --box-shadow: 0 3px 3px rgba(0, 0, 0, 0.3);
    --box-shadow-hover: 0 3px 3px rgba(0, 0, 0, 0.5);

    --font: "Secular One", sans-serif;
  }
</style>
