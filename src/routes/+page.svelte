<script>
    import Button from "../button.svelte";
    import StartMenu from "../startMenu.svelte";
    import pdfUrl from "$lib/assets/LG_CV.pdf";

    export let active = false;

    function handleClick() {
        console.log("Clicked");
        active = !active;
    }
</script>

<div class="container">
    <div class="content">
        <iframe src={pdfUrl} width="100%" height="600px" title="PDF Viewer"
        ></iframe>
    </div>

    {#if active}
        <div class="startButtonContent">
            <StartMenu />
        </div>
    {/if}
</div>
<div class="navbar">
    <div class="navbarContent">
        <Button on:click={handleClick} {active}>Start</Button>
    </div>
</div>

<style>
    .container {
        width: 99vw;
        height: 94vh;
    }
    .startButtonContent {
        background-color: #bab8b8;
        height: calc(30vh - 43px);
        bottom: 43px;
        left: 0vw;
        position: fixed;
        z-index: 1000;
        width: 13vw;
        border-left: 2px solid #eae9e9;
        border-top: 2px solid #eae9e9;
        border-right: 2px solid #656363;
        border-bottom: 2px solid #656363;
    }
    .content {
        background-color: #bab8b8;
        height: 75vh;
        width: 60vw;
        align-items: center;
        padding: 0.3em;
        border-left: 2px solid #eae9e9;
        border-top: 2px solid #eae9e9;
        border-right: 2px solid #656363;
        border-bottom: 2px solid #656363;
    }
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

    h1 {
        background-color: #797777;
        margin: 0;
        padding-left: 10px;
        color: white;
        font-family: "Segoe UI", sans-serif;
        font-weight: 100;
    }

    p {
        font-family: "Segoe UI", sans-serif;
        font-weight: 100;
        font-size: larger;
    }
</style>
