<script>
    export let active = false;
    export let width = "50px";
    export let buttonActive = false;
</script>

<button on:click class:active class:buttonActive style:width>
    <slot></slot>
</button>

<style>
    button {
        padding: 0.5rem 1rem;
        border-left: 1px solid #eae9e9;
        border-top: 1px solid #eae9e9;
        border-right: 1px solid #333232;
        border-bottom: 1px solid #333232;
        cursor: pointer;
        font-family: "Segoe UI", sans-serif;
        font-weight: 500;
        font-size: large;
        margin: 3px;
        display: flex;
        align-items: center;
        justify-content: center;
        height: 30px;
        box-shadow: 1px 1px 1px rgb(21, 20, 20);
    }
    button.active {
        background-color: #e7e3e3;
        box-shadow: none;
        border-left: 2px solid #5e5e5e;
        border-top: 2px solid #505050;
        border-right: 1px solid #eae9e9;
        border-bottom: 1px solid #eae9e9;
    }
    button.buttonActive {
        background-color: #e7e3e3;
        box-shadow: none;
        border-left: 2px solid #5e5e5e;
        border-top: 2px solid #505050;
        border-right: 1px solid #eae9e9;
        border-bottom: 1px solid #eae9e9;
    }
</style>
