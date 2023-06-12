<script>
  import { page } from "$app/stores";
  import Navbar from "../components/Navigation/Navbar.svelte";
</script>

<Navbar page={$page.url.pathname.replace("/", "") || "home"} />

<slot />

<style>
  :root {
    --bg-primary: rgb(239, 253, 255) 000;
    --bg-secondary: #f5f5f5;

    --primary: rgba(2, 145, 184, 1);
    --secondary: rgba(154, 218, 244, 1);

    --text: #272727;
    --text-muted: #626262;
  }
</style>
