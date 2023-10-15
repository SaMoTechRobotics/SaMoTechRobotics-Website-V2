<script>
    import {page} from "$app/stores";
    import Footer from "../components/Navigation/Footer.svelte";
    import Navbar from "../components/Navigation/Navbar.svelte";
</script>

<Navbar page={$page.url.pathname.replace("/", "") || "home"} home={$page.url.pathname === "/"}/>

<div class="content">
    <slot/>
</div>

<Footer/>

<style>
    @import url("https://fonts.googleapis.com/css2?family=Secular+One&display=swap");

    :root {
        --bg: rgb(239, 253, 255);
        --bg-hover: rgb(203, 222, 228);
        --bg-secondary: #f5f5f5;

        --primary: rgba(0, 200, 255, 1);
        --dark: rgba(2, 145, 184, 1);
        --secondary: rgb(77, 216, 254);

        --text: rgb(10, 100, 124);
        --text-gray: rgb(54, 89, 98);
        --text-muted: rgb(0, 139, 177);
        --text-inv: #fff;

        --text-shadow: 0 2px 2px rgba(0, 0, 0, 0.3);
        --text-shadow-hover: 0 3px 3px rgba(0, 0, 0, 0.3);
        --box-shadow: 0 3px 3px rgba(0, 0, 0, 0.3);
        --box-shadow-hover: 0 3px 3px rgba(0, 0, 0, 0.5);

        --img-shadow: 0 3px 3px rgba(0, 0, 0, 0.3);

        /*--font: "Secular One", sans-serif;*/
        --font: "Roboto", sans-serif;
    }

    .content {
        min-height: calc(100vh - 6rem - 5rem - 4rem);
    }
</style>
