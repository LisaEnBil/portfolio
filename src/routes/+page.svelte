<script lang="ts">
    import StartMenu from "../components/startMenu.svelte";
    import pdfUrl from "$lib/assets/LG_CV.pdf";
    import NavBar from "../components/navbar.svelte";

    let active = false;

    let selectedItems: string[] = [];

    let activeItem: string | null = null;
</script>

<div class="container">
    {#if activeItem}
        <div class="content">
            <p>{activeItem}</p>

            <!-- <iframe src={pdfUrl} width="100%" height="600px" title="PDF Viewer"
        ></iframe> -->
        </div>
    {/if}

    {#if active}
        <div class="startButtonContent">
            <StartMenu bind:selectedItems bind:activeItem />
        </div>
    {/if}
</div>
<NavBar bind:active bind:activeItem {selectedItems} />

<style>
    .container {
        width: 99vw;
        height: 94vh;
    }
    .startButtonContent {
        background-color: #bab8b8;
        height: calc(40vh - 43px);
        bottom: 43px;
        left: 0vw;
        position: fixed;
        width: 20vw;
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
</style>
