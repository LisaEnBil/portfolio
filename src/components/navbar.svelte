<script>
    import Button from "../components/button.svelte";

    export let active = false;
    export let selectedItems;

    function handleClick() {
        active = !active;
    }

    console.log("navbar", selectedItems);
</script>

<div class="navbar">
    <div class="navbarContainer">
        <Button on:click={handleClick} {active}>Start</Button>
        {#if selectedItems}
            {#each selectedItems as item}
                <div class="selectedItemBox">
                    <Button on:click={handleClick} {active}>{item}</Button>
                </div>
            {/each}
        {/if}
    </div>
</div>

<style>
    .navbar {
        display: flex;
        flex-direction: column;
        justify-content: end;
        position: fixed;
        height: auto;
        bottom: 0;
        left: 0;
        width: 100vw;
        z-index: 1000;
    }

    .navbarContainer {
        border-top: 2px solid #ded8d8;
        background-color: #bab8b8;
        height: 40px;
        width: 100vw;
        display: flex;
        flex-direction: row;
    }
    .navbarStart {
        border-top: 2px solid #ded8d8;
        background-color: #bab8b8;
        height: 40px;
        width: 100vw;
        display: flex;
        flex-direction: row;
    }
</style>
