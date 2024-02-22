<script>
  import { navigate } from "svelte-routing";
  export let Name = "";
  export let route = "";
  function handleClick() {
    navigate(route);
  }
</script>

<button class="btn" on:click={handleClick}>
  {Name}
</button>

<style>
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
