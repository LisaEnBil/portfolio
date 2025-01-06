<script lang="ts">
    import Button from "../components/button.svelte";

    export let active = false;
    export let selectedItems;

    export let activeItem: string | null = null;

    function handleClick() {
        active = !active;
    }

    /**
     * @param {any} item
     */
    function handleActiveClick(item: string) {
        const newActiveItem = activeItem === item ? null : item;
    }
</script>

<div class="navbar">
    <div class="navbarContainer">
        <Button on:click={handleClick} {active}>Start</Button>
        {#if selectedItems}
            {#each selectedItems as item}
                <div class="selectedItemBox">
                    <Button
                        on:click={() => handleActiveClick(item)}
                        width={"auto"}
                        buttonActive={activeItem === item}>{item}</Button
                    >
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
