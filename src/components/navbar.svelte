<script>
    import Button from "../components/button.svelte";
    import StartMenu from "../components/startMenu.svelte";
    import pdfUrl from "$lib/assets/LG_CV.pdf";
    import { createEventDispatcher } from "svelte";

    export let active = false;

    function handleClick() {
        active = !active;
    }
</script>

<div class="navbar">
    <div class="navbarContent">
        <Button on:click={handleClick} {active}>Start</Button>
    </div>
</div>

<style>
    .navbar {
        display: flex;
        flex-direction: column;
        justify-content: end;
        position: fixed;
        height: 23vh;
        bottom: 0;
        left: 0;
        width: 100vw;
        z-index: 1000;
    }

    .navbarContent {
        border-top: 2px solid #ded8d8;
        background-color: #bab8b8;
        height: 40px;
        width: 100vw;
        display: flex;
        flex-direction: row;
    }
</style>
