<script>
  import Navigation from "./Navigation.svelte";
  let src = "../static/cartoon.png";
  let name = "John Doe";
  let jobTitle = "Graphic Designer Extraordinaire";
</script>

<header>
  <div>
    <img {src} alt="{name} Avatar" />
    <div>
      <h1>{name}</h1>
      <h2>{jobTitle}</h2>
    </div>
  </div>
  <Navigation />
</header>

<style>
  header {
    background-image: url('../static/banner.jpg');
    padding: 10px;
    display: flex;
    flex-direction: column;
  }
  div {
    color: aliceblue;
    display: flex;
    flex-direction: row;
  }

  div > div {
    display: flex;
    flex-direction: column;
  }

  img {
    width: 100px;
    margin: 10px 20px 10px 20px;
  }

  h1 {
    font-size: 60px;
    margin: 0 0 10px 0;
    font-family: "Gemunu Libre", sans-serif;
  }

  h2 {
    font-size: 30px;
    margin: 0;
    font-family: "Gemunu Libre", sans-serif;
  }
</style>
