<script>
    import missingPiece from "$lib/assets/missingPiece.png";
</script>

<div class="container">
    <h1>Missing Piece: A Modern Take on the Classic Sliding Puzzle</h1>
    <h3>Android, Kotlin & Jetpack Compose</h3>
    <div class="content">
        <div class="technical">
            <h2>Key Features</h2>
            <li>Three difficulty levels to suit various skill levels</li>
            <li>High score tracking using Room database for local storage</li>
            <li>Smooth, responsive UI built with Jetpack Compose</li>

            <h2>Technical Highlights</h2>

            <p>
                Developed in Kotlin, leveraging modern Android development
                practices. Utilized Jetpack Compose for building the user
                interface, ensuring a fluid and interactive experience.
                Implemented Room database for efficient local data storage of
                high scores. User interface designed in Figma for a polished and
                intuitive look. Version control managed through Git and GitHub
                for streamlined development.
            </p>
        </div>

        <img
            width="150"
            height="300"
            class="image-margin rounded-corners"
            alt="Missing Piece screen shot"
            src={missingPiece}
        />
    </div>
</div>

<style>
    .container {
        height: 100%;
        width: 85%;
        align-items: flex-start;
    }
    .content {
        display: flex;
        flex-direction: row;
    }

    .technical {
        display: flex;
        flex-direction: column;
    }

    h1 {
        font-family: "Segoe UI", sans-serif;
        font-weight: 500;
    }

    h2 {
        font-family: "Segoe UI", sans-serif;
        font-weight: 500;
    }
    h3 {
        font-family: "Segoe UI", sans-serif;
        font-weight: 300;
    }
    li {
        margin-top: 10px;
        font-family: "Segoe UI", sans-serif;
        font-weight: 200;
    }
    p {
        font-family: "Segoe UI", sans-serif;
        font-weight: 100;
        font-size: large;
        margin: 0;
        margin-left: 10px;
    }
</style>
