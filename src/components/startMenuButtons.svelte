<script lang="ts">
    import logo from "$lib/assets/icons8-linkedin-48.png";
    import missingPiece from "$lib/assets/Component18.png";
    import fiffigaFrun from "$lib/assets/testIcon.png";
    import cheerMeApp from "$lib/assets/IMG_0045.jpg";
    import folder from "$lib/assets/folderFilled.png";

    export let selectedItems: string[] = [];

    export let activeItem: string | null = null;
    export let closeMenu: () => void;

    function handleItemClick(item: string) {
        if (item !== "LinkedIn") {
            activeItem = activeItem === item ? null : item;
            const event = new CustomEvent("itemSelect", {
                detail: selectedItems,
            });
            dispatchEvent(event);
            closeMenu();
        }
    }
</script>

<div class="menuList">
    <a href="https://www.linkedin.com/in/lisa-gillfrost/">
        <img width="50" height="50" alt="LinkedIn Icon" src={logo} />
        <p>LinkedIn</p>
    </a>
    <button
        on:click={() => {
            handleItemClick("Fiffiga Frun");
        }}
    >
        <img
            width="35"
            height="35"
            class="image-margin rounded-corners"
            alt="Fiffiga Frun App Icon"
            src={fiffigaFrun}
        />
        <p>Fiffiga Frun</p>
    </button>
    <button
        on:click={() => {
            handleItemClick("CheerMeApp");
        }}
    >
        <img
            width="35"
            height="35"
            class="image-margin rounded-corners"
            alt="Cheer Me App Icon"
            src={cheerMeApp}
        />
        <p>CheerMeApp</p>
    </button>
    <button
        class="bottom-image"
        on:click={() => {
            handleItemClick("Missing Piece");
        }}
    >
        <img
            class="image-margin"
            width="35"
            height="35"
            alt="Missing Piece Icon"
            src={missingPiece}
        />
        <p>Missing Piece</p>
    </button>
    <button
        on:click={() => {
            handleItemClick("Resume");
        }}
    >
        <img width="35" height="35" alt="Resume" src={folder} />
        <p>Resume</p>
    </button>
</div>

<style>
    .image-margin {
        margin-left: 5px;
    }
    .rounded-corners {
        border-radius: 15%;
    }
    .menuList {
        display: flex;
        flex-direction: column;
        height: 100%;
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
    @media screen and (max-width: 750px) {
        button {
            background-color: #bab8b800;
            color: #000000;
        }
        a {
            display: flex;
            justify-content: center;
            flex-direction: column;
            align-items: center;
            padding: 0;
        }
    }
    button {
        display: flex;
        border: none;
        margin-bottom: 5px;
        justify-content: center;
        width: 100%;
        flex-direction: column;
        align-items: center;
    }
    /* #010649 */
    p {
        font-family: "Segoe UI", sans-serif;
        font-weight: 100;
        font-size: small;
        margin: 0;
        margin-left: 10px;
        color: #000000;
    }
</style>
