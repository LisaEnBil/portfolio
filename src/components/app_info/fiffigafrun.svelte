<script>
    import fiffigaFrun from "$lib/assets/fiffigaFrunScreenShot.png";
</script>

<div class="container">
    <h1>Fiffiga Frun: Your Roadmap for Living Smarter</h1>
    <h3>iOS, React Native</h3>
    <p>
        Fiffiga Frun is a comprehensive mobile application that offers users
        hundreds of practical tips and life hacks, ranging from household
        cleaning techniques to travel shortcuts. Developed using React Native
        with TypeScript, this app provides a seamless and efficient user
        experience.
    </p>
    <div class="content">
        <div class="technical">
            <h2>Key Features</h2>

            <li>
                Extensive Database: Houses several hundred tips covering various
                aspects of daily life.
            </li>
            <li>
                Smart Search: Users can easily find specific tips using the
                search functionality.
            </li>
            <li>
                Category Filtering: Tips are organized into categories for quick
                access.
            </li>
            <li>
                User Contributions: Allows users to email their own tips,
                fostering community engagement.
            </li>
            <h2>Technical Highlights</h2>
            <p>
                Built with React Native and TypeScript for robust, type-safe
                development. User interface designed in Figma for a polished and
                intuitive look. Integrated Google AdMob for in-app advertising.
                Implemented RevenueCat for efficient management of paywalls and
                in-app purchases.
            </p>
        </div>

        <img
            width="150"
            height="300"
            class="image-margin rounded-corners"
            alt="Missing Piece screen shot"
            src={fiffigaFrun}
        />
    </div>
</div>

<style>
    .container {
        height: 100%;
        width: 60vw;
        align-items: flex-start;
        padding-left: 2em;
        padding-right: 2em;
        padding-bottom: 2em;
    }
    .content {
        display: flex;
        flex-direction: row;
    }

    .technical {
        display: flex;
        flex-direction: column;
        padding-bottom: 10px;
    }
    img {
        padding-top: 5px;
        padding-left: 5px;
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
