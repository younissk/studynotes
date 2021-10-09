<script>
  import { articles, getArticles, subjects } from "../fb";
  import Styledbutton from "../components/button.svelte";
  let pathsArray = window.location.pathname.split("/").filter((el) => el != "");

  getArticles(pathsArray[0], pathsArray[1]);

  function getRandomColor() {
    var letters = "0123456789ABCDEF";
    var color = "";
    for (var i = 0; i < 6; i++) {
      color += letters[Math.floor(Math.random() * 16)];
    }
    return color;
  }
</script>

<main>
  <h1>{pathsArray[1].replace("_", " ")}</h1>

  <p>
    {#each $subjects as subject}
      {#if subject.name === pathsArray[1]}
        {subject.intro}
      {/if}
    {/each}
  </p>

  <div class="buttons">
    {#each $articles as article}
      <Styledbutton
        path={`${pathsArray[0]}/${pathsArray[1]}/${article.id}`}
        color={getRandomColor()}
        name={article.data().name}
      />
    {/each}
  </div>
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Ubuntu:wght@300&display=swap");
  h1 {
    color: #f02d35;
  }

  /* h1:focus {
    outline: none;
  } */

  p {
    font-weight: bolder;
    width: 70vw;
  }

  * {
    font-family: "ubuntu", sans-serif;
    letter-spacing: 0.3vw;
  }
  main {
    margin: 50px;
  }

  .buttons {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
    margin: 20px 0px;
  }
</style>
