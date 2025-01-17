<!-- HamburgerButton.svelte -->
<script lang="ts">
    export let onClick: () => void;
</script>

<button on:click={onClick} class="hamburger-button">
    <span></span>
    <span></span>
    <span></span>
</button>

<style>
    .hamburger-button {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        width: 30px;
        height: 25px;
        background: transparent;
        border: none;
        cursor: pointer;
        padding: 0;
    }

    .hamburger-button span {
        width: 30px;
        height: 3px;
        background: #000;
    }
</style>
