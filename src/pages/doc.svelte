<script>
  import { fbGetDocument, htmlDocument } from "../fb";
  let pathsArray = window.location.pathname.split("/").filter((el) => el != "");

  fbGetDocument(pathsArray[0], pathsArray[2]);
</script>

<main>
  <article>
    {@html $htmlDocument}
  </article>
</main>

<style>
  article {
    padding-bottom: 10vh !important;
  }
</style>
