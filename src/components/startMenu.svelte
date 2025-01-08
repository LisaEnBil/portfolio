<script lang="ts">
    import logo from "$lib/assets/icons8-linkedin-48.png";
    import missingPiece from "$lib/assets/Component18.png";
    import fiffigaFrun from "$lib/assets/testIcon.png";
    import cheerMeApp from "$lib/assets/IMG_0045.jpg";
    import folder from "$lib/assets/folderFilled.png";

    export let selectedItems: string[] = [];

    export let activeItem: string | null = null;

    const menuItems = [
        { name: "Fiffiga Frun", icon: fiffigaFrun },
        { name: "CheerMeApp", icon: cheerMeApp },
        { name: "Missing Piece", icon: missingPiece },
    ];

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
    <div class="graySpace"></div>
    <div class="menuList">
        <a href="https://www.linkedin.com/in/lisa-gillfrost/">
            <div class="rowContent">
                <img width="48" height="48" alt="LinkedIn Icon" src={logo} />
                <p>LinkedIn</p>
            </div>
        </a>
        {#each menuItems as item}
            <button
                on:click={() => {
                    handleItemClick(item.name);
                }}
            >
                <div class="rowContent">
                    <img
                        width="35"
                        height="35"
                        class="image-margin rounded-corners"
                        alt="Fiffiga Frun App Icon"
                        src={item.icon}
                    />
                    <p class="text-margin">{item.name}</p>
                </div>
            </button>
        {/each}
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
    .text-margin {
        margin-left: 15px;
    }
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
        width: 100%;
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
