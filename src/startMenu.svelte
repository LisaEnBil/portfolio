<script>
    import logo from "$lib/assets/icons8-linkedin-48.png";
    import missingPiece from "$lib/assets/Component18.png";
    import fiffigaFrun from "$lib/assets/testIcon.png";
    import cheerMeApp from "$lib/assets/IMG_0045.jpg";
</script>

<div class="menu">
    <div class="graySpace"><p>""</p></div>
    <div class="menuList">
        <div class="appList">
            <a href="https://www.linkedin.com/in/lisa-gillfrost/">
                <div class="rowContent">
                    <img alt="LinkedIn Icon" src={logo} />
                    <p>LinkedIn</p>
                </div>
            </a>
            <a href="https://www.linkedin.com/in/lisa-gillfrost/">
                <div class="rowContent">
                    <img
                        width="38"
                        height="38"
                        class="bottom-image"
                        alt="Missing Piece Icon"
                        src={missingPiece}
                    />
                    <p>Missing Piece</p>
                </div>
            </a>
            <a href="https://www.linkedin.com/in/lisa-gillfrost/">
                <div class="rowContent">
                    <img
                        width="38"
                        height="38"
                        class="bottom-image fiffiga-frun"
                        alt="Fiffiga Frun App Icon"
                        src={fiffigaFrun}
                    />
                    <p>Fiffiga Frun</p>
                </div>
            </a>
            <a href="https://www.linkedin.com/in/lisa-gillfrost/">
                <div class="rowContent">
                    <img
                        width="38"
                        height="38"
                        class="bottom-image fiffiga-frun"
                        alt="Fiffiga Frun App Icon"
                        src={cheerMeApp}
                    />
                    <p>Cheer Me App</p>
                </div>
            </a>
        </div>
        <div class="resume"></div>
    </div>
</div>

<style>
    .appList {
        border-bottom: 2px solid #656363;
    }
    .resume {
        border-top: 2px solid #eae9e9;
    }
    .bottom-image {
        padding-left: 5px;
        padding-right: 5px;
        padding-top: 5px;
    }
    .fiffiga-frun {
        border-radius: 20%;
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
