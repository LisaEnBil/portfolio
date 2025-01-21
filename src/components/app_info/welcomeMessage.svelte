<script lang="ts">
    import Button from "../button.svelte";

    export let activeItem: string | null = null;
    export let selectedItems: string[] = [];

    function handleClose() {
        selectedItems =
            selectedItems && selectedItems.filter((i) => i !== activeItem);
        activeItem = null;
    }
</script>

<div class="container">
    <div class="title">
        <h1>Welcome to my <b>Portfolio</b></h1>
    </div>

    <div class="text-content">
        <p>
            Every line of code tells a story. Browse through my curated
            collection of projects, each representing a challenge solved, a
            problem innovated, and a skill mastered. Your journey begins with a
            click on the start menu.
        </p>
    </div>
    <div class="bottom">
        <div class="button-wrapper">
            <Button on:click={handleClose} width={150}>
                <div class="button-text-wrapper">
                    <p class="button-text">Close</p>
                </div>
            </Button>
        </div>
    </div>
</div>

<style>
    .button-wrapper {
        margin-right: 1em;
    }
    .button-text-wrapper {
        width: 97%;
        height: 85%;
        border: 2px dotted #414040;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .button-text {
        margin: 0;
        padding: 0;
        font-weight: 500;
    }
    .bottom {
        width: 100%;
        display: flex;
        justify-content: flex-end;
        padding-top: 1em;
        padding-bottom: 1em;
    }
    .container {
        height: 100%;
        width: 37vw;
        display: flex;
        align-items: flex-start;
        margin-left: 2em;
    }
    .text-content {
        display: flex;
        background-color: #d2d2a9;
        border-left: 2px solid #656363;
        border-top: 2px solid #656363;
        border-right: 2px solid #eae9e9;
        border-bottom: 2px solid #eae9e9;
        width: 29em;
        height: 20em;
        justify-content: center;
        align-items: center;
    }
    .title {
        display: flex;
        flex-direction: row;
        align-items: center;
        width: 200;
    }

    h1 {
        font-family: "Segoe UI", serif;
        font-weight: 600;
    }
    b {
        font-family: "Segoe UI", sans-serif;
        font-weight: 800;
    }
    p {
        font-family: "Segoe UI", sans-serif;
        font-weight: 200;
        font-size: medium;
        margin: 0;
        margin-left: 30px;
        margin-right: 30px;
    }
</style>
