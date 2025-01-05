<script>
    import Button from "../components/button.svelte";

    export let active = false;
    export let selectedItem = "";

    function handleClick() {
        active = !active;
    }
</script>

<div class="navbar">
    <div class="navbarStart">
        <Button on:click={handleClick} {active}>Start</Button>
    </div>
    <div>
        {#if selectedItem}
            <div class="selectedItemBox">
                <p>{selectedItem}</p>
            </div>
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

    .navbarStart {
        border-top: 2px solid #ded8d8;
        background-color: #bab8b8;
        height: 40px;
        width: 100vw;
        display: flex;
        flex-direction: row;
    }
</style>
