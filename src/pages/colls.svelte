<script>
  import Styledbutton from "../components/button.svelte";
</script>

<main>
  <h1>Study Notes</h1>
  <p>
    On this site, I leave all of my notes that I gather while studying. Look
    around and see if they might benefit you!
  </p>
  <div class="buttons">
    <Styledbutton
      path="Web_Development"
      color="FBD283"
      name="Web Dev"
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c4/Globe_icon.svg/1024px-Globe_icon.svg.png"
    />
    <Styledbutton
      path="Paramedic"
      color="ED1639"
      name="Sanitäter"
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/57/Logo_ASB%C3%96.svg/1200px-Logo_ASB%C3%96.svg.png"
    />
    <!-- <Styledbutton
      path="Language"
      color="FE9C53"
      name="Language"
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/43/OOjs_UI_icon_language-ltr.svg/1024px-OOjs_UI_icon_language-ltr.svg.png"
    />
    <Styledbutton
      path="Knowledge"
      color="F76242"
      name="Knowledge"
      src="https://cdn.iconscout.com/icon/free/png-256/islam-100384.png"
    /> -->
    <!-- <Styledbutton
      path="Design"
      color="F02D35"
      name="Design"
      src="https://www.svgrepo.com/show/148917/website-design.svg"
    /> -->
  </div>
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Ubuntu:wght@300&display=swap");
  h1 {
    color: #f02d35;
  }

  h1:focus {
    outline: none;
  }

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
