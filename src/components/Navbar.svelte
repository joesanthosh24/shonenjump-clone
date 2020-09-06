<script>
  import Icon from "svelte-awesome";
  import { heart, search, shoppingCart } from "svelte-awesome/icons";
</script>

<style>
   #navbar {
    display: flex;
    width: 100%;
    overflow: hidden;
    transition: color 2ms ease-in;
  }
  .navbarLeft {
    background-color: #F2F2F2;
    padding-left: 20px;
    flex: 0.8;
  }
  .navbarRight {
    background-color: red;
    text-align: left;
    flex: 0.2;
    height: 113px;
  }
  .navbarRight > img {
    object-fit: contain;
    height: 80px;
    width: 120px;
    padding-left: 10%;
    padding-top: 5%;
  }
  .top {
    display: flex;
    justify-content: space-between;
    margin-top: 15px;
  }
  .topLink {
    padding: 10px;
    color: #2e2e2e;
    font-size: 20px;
  }
  .topLink:hover {
    color: #FF0000;
  }
  .bottom {
    margin-top: 20px;
  }
  .bottomLink {
    padding: 10px 15px;
    color: #2e2e2e;
    font-size: 26px;
    font-weight: 700;
    text-transform: uppercase;
  }
  .bottomLink:hover {
    color: #FF0000;
  }
  .active {
    border-bottom: 5px solid #2e2e2e;
  }
  .inputContainer {
    display: flex;
    align-items: center;
    border: 1px solid #fff;
    padding: 7px;
    background-color: #fff;
    margin-right: 50px;
  }
  input {
    border: none;
    flex: 1;
    width: 250px;
  }
  input:focus {
    outline: none;
  }

  /* Media Queries */
  @media (min-width: 1500px) {
    .navbarLeft {
      padding-left: 50px;
    }
  }
  @media (min-width: 1700px) {
    .navbarLeft {
      padding-left: 100px;
    }
  }
  @media (min-width: 1900px) {
    .navbarLeft {
      padding-left: 300px;
    }
  }
</style>

<nav id="navbar">
  <div class="navbarLeft">
    <div class="top">
      <div class="topLinks">
        <a href="#" id="first-top-link" class="topLink">Log In</a>
        <a href="#" class="topLink">Sign Up</a>
        <a href="#" class="topLink">
          <Icon data={heart} />
        </a>
        <a href="#" class="topLink">
          <Icon data={shoppingCart} />
        </a>
        <a href="#" class="topLink">My Library</a>
      </div>
      <div class="topInputContainer">
        <div class="inputContainer">
          <input type="text" placeholder="Find a Title or a Character..." />
          <Icon data={search} />
        </div>
      </div>
    </div>
    <div class="bottom">
      <a href="#" class="bottomLink">Read</a>
      <a href="#" class="bottomLink">Watch</a>
      <a href="#" class="bottomLink active">Shonen Jump</a>
      <a href="#" class="bottomLink">Community</a>
      <a href="#" class="bottomLink">Calender</a>
    </div>
  </div>
  <div class="navbarRight">
    <img
      src="https://assets.viz.com/assets/logo@2x-b76f649f933ea15f45147ff5445a2501c85c7f863ba0aba5ea7bec93c3272cc6.png"
      alt="Viz Logo" />
  </div>
</nav>
