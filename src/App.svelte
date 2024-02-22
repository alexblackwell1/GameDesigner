<script>
  import { Router, Route, Link } from "svelte-routing";
  import Button from "./Components/Button.svelte";
  import Developers from "./Pages/DeveloperLanding.svelte";
  // import Players from "./Pages/PlayerLanding.svelte";

  let title = "Board Game Developer";
  let description = "Board game Developer Home Page";
  let keywords = "Board Game, Developer, Player";
  let author = "Alex B.";
</script>

<svelte:head>
  <title>{title}</title>
  <meta charset="UTF-8" />
  <meta name="description" content={description} />
  <meta name="keywords" content={keywords} />
  <meta name="author" content={author} />
  <link rel="stylesheet" type="text/css" href="styles.css" />
</svelte:head>

<Router>
  <div id="vertical-container">
    <header>
      <h1>Hark!</h1>
    </header>

    <main>
      <div><Button Name="Welcome Developers" route="/developers" /></div>
      <div><Button Name="Welcome Players" /></div>
    </main>
  </div>

  <footer>
    <p>Copyright © 2024 {author}</p>
  </footer>

  <Route path="/developers" component={Developers} />
</Router>

<style>
  :root {
    background-color: #031526;
    height: 100vh;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  #vertical-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 80vh;
  }

  header {
    color: #e9d985;
  }

  header,
  main {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  main div {
    padding: 1vh;
  }

  footer {
    position: fixed;
    left: 0;
    bottom: 0;
    width: 100%;
    text-align: center;
  }
</style>
