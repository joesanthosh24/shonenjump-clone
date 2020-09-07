<script>
  import Manga from "./Manga.svelte";

  import { baseUrl } from "../api";

  let mangas = [];

  fetch(baseUrl)
    .then((res) => res.json())
    .then((data) => {
      const mangaData = data.data;

      mangaData.map((manga) => {
        mangas = [...mangas, { id: manga.id, data: manga.attributes }];
      });
    });

  console.log(mangas);
</script>

<style>
  h3 {
    font-weight: 700;
    font-size: 56px;
  }
  h4 {
    line-height: 1;
    font-size: 35px;
    font-weight: lighter;
  }
  .containerBgImg {
    background: url("https://de7i3bh7bgh0d.cloudfront.net/wsj-bg-smoketile.jpg");
    height: 800px;
    width: 100%;
  }
  .mangaContent {
    background-color: #f2f2f2;
    text-align: left;
    width: 100%;
  }
  .headerContent {
    padding-top: 8%;
  }
  .item {
    margin-left: 10px;
    margin-right: 5px;
    color: #949494;
    font-size: 28px;
  }
  #first-item {
    cursor: not-allowed;
    color: #cccccc;
    margin-left: 25px;
  }
  .logo {
    text-align: center;
    margin: 10px 90px;
  }
  img {
    object-fit: contain;
    width: 100%;
  }
  .chapterText {
    margin-left: 25px;
    color: #2e2e2e;
  }
  .mangas {
    margin-left: 25px;
    margin-top: 40px;
    display: flex;
    flex-wrap: wrap;
  }

  /* Media Queries */
  @media (min-width: 1367px) {
    .mangaContent {
      width: 75%;
      margin: 0 12.5%;
    }
  }
</style>

<div class="containerBgImg">
  <div class="mangaContent">
    <!-- Header Content -->
    <div class="headerContent">
      <a href="#" id="first-item" class="item">Shonen Jump</a> | <a
        href="#"
        class="item">Chapter Schedule</a> | <a href="#" class="item">Comment</a>
      | <a href="#" class="item">Blog</a> | <a href="#" class="item">New Volumes</a>
    </div>
    <!-- Shonen Jump Logo -->
    <div class="logo">
      <img
        src="https://dw9to29mmj727.cloudfront.net/SJ/sj-logo-wide.png"
        alt="Shonen Logo" />
    </div>
    <!-- Latest Chapters Text -->
    <div class="chapterText">
      <h3>LATEST FREE CHAPTERS</h3>
      <h4>
        Coming Sunday: New series <em>High School Family</em>! Imagine if your
        whole family ended up being your classmates!
      </h4>
    </div>
    <!-- List of Manga -->
    <div class="mangas">
      {#each mangas as { id, data: { titles, posterImage: { original, tiny, small, medium, large }, chapterCount } }}
        <Manga
          {id}
          {titles}
          imageUrl={original || tiny || small || medium || large}
          chapters={chapterCount} />
      {/each}
    </div>
  </div>
</div>
