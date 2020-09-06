<script>
  export let id;
  export let titles;
  export let imageUrl;

  let defaultImageUrl =
    "https://is1-ssl.mzstatic.com/image/thumb/Purple124/v4/33/f6/24/33f624ec-d804-9105-f2c5-b428edc8a6bf/contsched.mktjdkux.png/600x600wa.png";
</script>

<style>
  .mangaContainer {
    width: 300px;
    height: 350px;
    background-color: #2e2e2e;
    margin-right: 30px;
    margin-bottom: 30px;
  }
  .mangaContainer:hover {
    background-color: red;
  }
  img {
    width: 100%;
    height: 70%;
  }
  .mangaDescription {
    text-align: center;
    margin: 0;
    width: 100%;
    height: 30%;
  }
  h4 {
    font-size: 23px;
    color: white;
  }
</style>

<!-- <p id={id}>{titles.en_us || titles.en_jp}</p> -->
<div id={id} class="mangaContainer">
  <img src={imageUrl || defaultImageUrl} alt="Manga Poster" />
  <div class="mangaDescription">
    <h4>{titles.en_us || titles.en_jp}</h4>
  </div>
</div>
