<script>
  let headlinedAnimes = [
    "Demon Slayer",
    "Sailor Moon",
    "My Hero Academia",
    "Naruto",
    "Boruto",
    "Pokemon",
    "One Punch Man",
  ];
</script>

<style>
  #header {
    display: flex;
    background-color: #2e2e2e;
    font-family: "Circular", Avenir, sans-serif;
  }
  #first_item {
    margin-left: 10%;
    color: #949494;
  }
  .item {
    padding: 10px;
    font-size: 16px;
    color: #d8d8d8;
  }
  .item:hover {
    color: white;
  }
  #last_item {
    margin-right: auto;
  }
  a {
    text-decoration: none;
  }
</style>

<div id="header">
  <p class="item" id="first_item">Manga & Anime Favorites</p>
  {#each headlinedAnimes as anime}<a href="#" class="item">{anime}</a>{/each}
  <a class="item" href="#" id="last_item">Free Manga</a>
</div>
