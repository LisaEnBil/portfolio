<script lang="ts">
    import StartMenu from "../components/startMenu.svelte";
    import Fiffigafrun from "../components/app_info/fiffigafrun.svelte";
    import Resume from "../components/app_info/resume.svelte";
    import MissingPiece from "../components/app_info/missingPiece.svelte";
    import CheerMeApp from "../components/app_info/cheermeapp.svelte";
    import NavBar from "../components/navbar.svelte";

    let active = false;
    let selectedItems: string[] = [];
    let activeItem: string | null = null;
</script>

<div class="container">
    {#if activeItem}
        <div class="content">
            <div class="header"><p>{activeItem}</p></div>
            {#if activeItem === "Fiffiga Frun"}
                <Fiffigafrun />
            {:else if activeItem === "Resume"}
                <Resume />
            {:else if activeItem === "Missing Piece"}
                <MissingPiece />
            {:else if activeItem === "CheerMeApp"}
                <CheerMeApp />
            {/if}
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
        width: 15vw;
        border-left: 2px solid #eae9e9;
        border-top: 2px solid #eae9e9;
        border-right: 2px solid #656363;
        border-bottom: 2px solid #656363;
    }
    .content {
        display: flex;
        flex-direction: column;
        background-color: #bab8b8;
        height: 75vh;
        width: 60vw;
        align-items: center;
        border-left: 2px solid #eae9e9;
        border-top: 2px solid #eae9e9;
        border-right: 2px solid #656363;
        border-bottom: 2px solid #656363;
    }
    .header {
        height: 20px;
        background-color: #787878;
        width: 100%;
        display: flex;
        align-items: center;
    }
    p {
        font-family: "Segoe UI", sans-serif;
        color: #ffffff;
        font-weight: 100;
        margin: 0;
        padding-left: 5px;
        font-size: smaller;
    }
</style>
