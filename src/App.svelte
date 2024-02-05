<script>
  import { onMount } from "svelte";

  onMount(() => {
    document.body.style.backgroundColor = "#031526";
  });
</script>

<main>
  <h1>Hello Player!</h1>
  <button class="btn">Log In</button>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #e9d985;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  .btn {
    text-decoration: none;
    border: 1px solid #bcd8c1;
    background-color: #007991;
    position: relative;
    overflow: hidden;
    border-radius: 3em;
    padding: 0.5em 5em;
    color: #e9d985;
  }

  .btn:hover {
    box-shadow: 1px 1px 25px 10px #bcd8c140;
  }

  .btn:before {
    content: "";
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(120deg, transparent, #bcd8c1, transparent);
    transition: all 650ms;
  }

  .btn:hover:before {
    left: 100%;
  }
</style>
