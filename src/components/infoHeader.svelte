<script lang="ts">
    import closeIcon from "$lib/assets/icons8-multiply-30.png";

    export let activeItem: string | null = null;
    export let selectedItems: string[] | null = [];

    export function handleXClick() {
        selectedItems =
            selectedItems && selectedItems.filter((i) => i !== activeItem);
        activeItem = null;
    }
</script>

<div class="header">
    <p>{activeItem}</p>

    <button on:click={handleXClick}>
        <img
            width="15"
            height="15"
            class="image-margin rounded-corners"
            alt="Close content"
            src={closeIcon}
        />
    </button>
</div>

<style>
    .header {
        height: 30px;
        background-color: #787878;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    button {
        background-color: #bab8b8;
    }
    p {
        font-family: "Segoe UI", sans-serif;
        color: #ffffff;
        font-weight: 100;
        margin: 0;
        padding-left: 5px;
        font-size: medium;
    }
</style>
