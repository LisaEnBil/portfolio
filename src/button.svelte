<script>
    export let active = false;
</script>

<button on:click class:active>
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
        width: 50px;
        box-shadow: 1px 1px 1px rgb(21, 20, 20);
    }
    button.active {
        background-color: #e7e3e3;
        border: 1px solid #626060;
        box-shadow: none;
    }
</style>
