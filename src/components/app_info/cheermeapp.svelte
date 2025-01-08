<script>
    import cheerMeApp from "$lib/assets/cheerMeApp.png";
</script>

<div class="container">
    <h1>CheerMeApp: Your Virtual Feline Companion</h1>
    <h3>iOS, SwiftUI</h3>

    <p>
        Interactive Cat Scratching: Users can scratch a virtual cat on their
        device screen, triggering a realistic purring sound. The app utilizes
        haptic feedback to simulate the sensation of a cat's vibration, creating
        a multi-sensory experience.
    </p>
    <div class="content">
        <div class="column-content">
            <h2>Personalized Cat Library</h2>
            <p>
                CheerMeApp allows users to add their own cats to the app's
                library. This feature enables pet owners to:
            </p>
            <li>Choose an existing photo or take a new one of their cat.</li>
            <li>Record their cat's unique purring sound.</li>
            <li>Bring their beloved virtual cat on vacations.</li>

            <h2>Technical Highlights</h2>
            <p>
                Developed using SwiftUI, leveraging the latest iOS features.
                Implemented Firebase Authentication for secure user access.
                Utilized Firebase Storage for efficient media management.
                Employed Firebase Database for robust data handling. Designed
                user interface with Figma for a polished look. Version control
                managed through Git and GitHub
            </p>
        </div>
        <img
            width="150"
            height="300"
            class="image-margin rounded-corners"
            alt="Missing Piece screen shot"
            src={cheerMeApp}
        />
    </div>
</div>

<style>
    .container {
        height: auto;
        width: 85%;
        align-items: flex-start;
    }
    .content {
        display: flex;
        flex-direction: row;
    }
    .column-content {
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
    img {
        padding-top: 5px;
        padding-left: 5px;
    }

    p {
        font-family: "Segoe UI", sans-serif;
        font-weight: 100;
        font-size: large;
        margin: 0;
        margin-left: 10px;
    }
</style>
