<script lang="ts">
    import StartMenu from "../components/startMenu.svelte";
    import Fiffigafrun from "../components/app_info/fiffigafrun.svelte";
    import Resume from "../components/app_info/resume.svelte";
    import MissingPiece from "../components/app_info/missingPiece.svelte";
    import CheerMeApp from "../components/app_info/cheermeapp.svelte";
    import NavBar from "../components/navbar.svelte";
    import InfoHeader from "../components/infoHeader.svelte";
    import { onMount } from "svelte";
    import StartMenuButtons from "../components/startMenuButtons.svelte";
    import HamburgerMenu from "../components/hamburgerMenu.svelte";

    let active = false;
    let selectedItems: string[] = [];
    let activeItem: string | null = null;

    let buttonMenuActive = false;

    let screenWidth: number;

    function toggleMenu() {
        buttonMenuActive = !buttonMenuActive;
    }

    onMount(() => {
        screenWidth = window.innerWidth;
        window.addEventListener("resize", () => {
            screenWidth = window.innerWidth;
        });
    });

    $: isMobile = screenWidth <= 750;
</script>

<div class="container">
    {#if isMobile}
        <div class="hamburger-menu">
            <HamburgerMenu onClick={toggleMenu} />
        </div>
    {/if}
    {#if isMobile && buttonMenuActive}
        <div class="stuff">
            <StartMenuButtons
                bind:selectedItems
                bind:activeItem
                closeMenu={() => (buttonMenuActive = false)}
            />
        </div>
    {/if}

    {#if activeItem}
        <div class="content">
            <InfoHeader bind:selectedItems bind:activeItem />
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

    {#if !isMobile && active}
        <div class="startButtonContent">
            <StartMenu bind:selectedItems bind:activeItem bind:active />
        </div>
    {/if}
</div>
{#if !isMobile}
    <NavBar bind:active bind:activeItem {selectedItems} />
{/if}

<style>
    .hamburger-menu {
        position: fixed;
        top: 10px;
        right: 10px;
        z-index: 1001;
    }
    .stuff {
        position: fixed;
        top: 50px;
        right: 10px;
        z-index: 1001;
    }
    .startButtonContent {
        background-color: #bab8b8;
        height: calc(40vh - 43px);
        bottom: 43px;
        left: 0vw;
        position: fixed;
        width: fit-content;
        border-left: 2px solid #eae9e9;
        border-top: 2px solid #eae9e9;
        border-right: 2px solid #656363;
        border-bottom: 2px solid #656363;
    }
    .content {
        display: flex;
        flex-direction: column;
        background-color: #bab8b8;
        height: auto;
        width: 60vw;
        align-items: center;
        border-left: 2px solid #eae9e9;
        border-top: 2px solid #eae9e9;
        border-right: 2px solid #656363;
        border-bottom: 2px solid #656363;
        margin-top: 60px;
    }
    @media screen and (max-width: 750px) {
        .container {
            display: flex;
            flex-direction: column;
            overflow-y: scroll;
        }
        .content {
            height: auto;
            width: auto;
            margin-top: 60px;
        }
    }
</style>
