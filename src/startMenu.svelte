<script>
    import logo from "$lib/assets/icons8-linkedin-48.png";
    import missingPiece from "$lib/assets/Component 18.png";
</script>

<div class="menu">
    <div class="graySpace"><p>""</p></div>
    <div class="menuList">
        <a href="https://www.linkedin.com/in/lisa-gillfrost/">
            <div class="rowContent">
                <img alt="LinkedIn Icon" src={logo} />
                <p>LinkedIn</p>
            </div>
        </a>
        <a href="https://www.linkedin.com/in/lisa-gillfrost/">
            <div class="rowContent">
                <enhanced:img
                    src={missingPiece}
                    alt="Description"
                    sizes="min(40px, 2vw)"
                />

                <p>LinkedIn</p>
            </div>
        </a>
    </div>
</div>

<style>
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
        flex-grow: 1;
    }
    .rowContent {
        display: flex;
        flex-direction: row;
        font-family: "Segoe UI", sans-serif;
        font-weight: 100;
    }
    .menuList a {
        text-decoration: none;
        color: inherit;
    }

    .menuList a:visited {
        color: inherit;
    }

    .menuList p::first-letter {
        text-decoration: underline;
    }
</style>
