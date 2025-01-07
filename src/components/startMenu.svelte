<script lang="ts">
    import logo from "$lib/assets/icons8-linkedin-48.png";
    import missingPiece from "$lib/assets/Component18.png";
    import fiffigaFrun from "$lib/assets/testIcon.png";
    import cheerMeApp from "$lib/assets/IMG_0045.jpg";
    import folder from "$lib/assets/folderFilled.png";

    export let selectedItems: string[] = [];

    export let activeItem: string | null = null;

    function handleItemClick(item: string) {
        if (item !== "LinkedIn") {
            const index = selectedItems.indexOf(item);
            if (index === -1) {
                selectedItems = [...selectedItems, item];
                activeItem = activeItem === item ? null : item;
            }
            const event = new CustomEvent("itemSelect", {
                detail: selectedItems,
            });
            dispatchEvent(event);
        }
    }
</script>

<div class="menu">
    <div class="graySpace"><p>""</p></div>
    <div class="menuList">
        <a href="https://www.linkedin.com/in/lisa-gillfrost/">
            <div class="rowContent">
                <img width="50" height="50" alt="LinkedIn Icon" src={logo} />
                <p>LinkedIn</p>
            </div>
        </a>
        <button
            on:click={() => {
                handleItemClick("Fiffiga Frun");
            }}
        >
            <div class="rowContent">
                <img
                    width="35"
                    height="35"
                    class="image-margin rounded-corners"
                    alt="Fiffiga Frun App Icon"
                    src={fiffigaFrun}
                />
                <p>Fiffiga Frun</p>
            </div>
        </button>
        <button
            on:click={() => {
                handleItemClick("CheerMeApp");
            }}
        >
            <div class="rowContent">
                <img
                    width="35"
                    height="35"
                    class="image-margin rounded-corners"
                    alt="Cheer Me App Icon"
                    src={cheerMeApp}
                />
                <p>CheerMeApp</p>
            </div>
        </button>
        <button
            class="bottom-image"
            on:click={() => {
                handleItemClick("Missing Piece");
            }}
            ><div class="rowContent">
                <img
                    class="image-margin"
                    width="35"
                    height="35"
                    alt="Missing Piece Icon"
                    src={missingPiece}
                />
                <p>Missing Piece</p>
            </div>
        </button>
        <button
            on:click={() => {
                handleItemClick("Resume");
            }}
            ><div class="rowContent">
                <img width="45" height="45" alt="Resume" src={folder} />
                <p>Resume</p>
            </div>
        </button>
    </div>
</div>

<style>
    .image-margin {
        margin-left: 5px;
    }
    .rounded-corners {
        border-radius: 15%;
    }
    .menu {
        border: 0.5px solid #656363;
        display: flex;
        flex-direction: row;
        width: 100%;
        height: 100vh;
    }
    .graySpace {
        display: flex;
        background-color: #797777;
        width: 20%;
        height: 100%;
    }
    .menuList {
        display: flex;
        flex-direction: column;
        height: 100%;
    }
    .rowContent {
        display: flex;
        align-items: center;
        flex-direction: row;
        font-family: "Segoe UI", sans-serif;
        font-weight: 100;
    }
    .menuList a {
        text-decoration: none;
        color: inherit;
        margin: 5px;
    }

    .menuList a:visited {
        color: inherit;
    }

    .menuList p::first-letter {
        text-decoration: underline;
    }
    button {
        background-color: #bab8b8;
        border: none;
        margin-bottom: 5px;
        justify-content: center;
    }
    /* #010649 */
    p {
        font-family: "Segoe UI", sans-serif;
        font-weight: 100;
        font-size: small;
        margin: 0;
        margin-left: 10px;
    }
</style>
