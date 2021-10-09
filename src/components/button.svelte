<script>
  import { Link } from "svelte-navigator";
  export let src = "";
  export let name = "test";
  export let color = "FBD283";
  export let path = "/Web_Development";
</script>

<Link
  to="/{path}"
  style="font-family: 'ubuntu', sans-serif;text-decoration: none;color: black;font-weight: bolder;"
>
  <div class="button" style="background-color: #{color};">
    {#if src !== "" || src === undefined}
      <img {src} alt="" class="icon" />
    {/if}
    <h3>{name}</h3>
  </div>
</Link>

<style>
  /* Link {
		font-family: 'ubuntu', sans-serif;
		text-decoration: none;
		color: black;
		font-weight: bolder;
	} */

  .button {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-evenly;
    margin: 0px 10px 10px 0px;
    padding: 15px 0px;
    border-radius: 15px;
  }

  h3 {
    margin: 0px;
    padding: 0px;
    font-size: 16px;
    color: black !important;
  }

  img {
    width: 10%;
  }
</style>
