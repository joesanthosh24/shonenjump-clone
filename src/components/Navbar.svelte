<script>
  import Icon from "svelte-awesome";
  import { heart, search, shoppingCart } from "svelte-awesome/icons";
</script>

<style>
  #navbar {
    display: flex;
    width: 100%;
    overflow: hidden;
  }
  .navbarLeft {
    flex: 0.8;
    background-color: #F2F2F2;
  }
  .navbarRight {
    background-color: red;
    flex: 0.2;
    text-align: left;
  }
  .navbarRight > img {
    object-fit: contain;
    height: 80px;
    width: 80px;
    margin: 5px auto;
    margin-left: 20px;
  }
  .top {
    display: flex;
    margin-left: 10%;
    padding: 20px;
    justify-content: space-between;
    align-items: center;
  }
  .topLinks {
    padding-left: 15px;
  }
  .topLink {
    margin-right: 15px;
    color: #2e2e2e;
    font-size: 20px;
    transition: color 2ms ease-in;
  }
  .topLink:hover {
    color: #FF0000;
  }
  .topInputContainer {
    flex: 0.4;
    display: flex;
  }
  .inputContainer {
    display: flex;
    align-items: center;
    border: 1px solid #fff;
    padding: 7px;
    background-color: #fff;
  }
  input {
    border: none;
    flex: 1;
    width: 250px;
  }
  input:focus {
    outline: none;
  }
  .bottom {
    text-transform: uppercase;
    padding-left: 140px;
    display: flex;
  }
  .bottomLink {
    margin-right: 15px;
    color: #2e2e2e;
    font-size: 26px;
    font-weight: 700;
    padding-bottom: 15px;
    transition: color 2ms ease-in;
  }
  .bottomLink:hover {
    color: #FF0000;
  }
  .active {
    border-bottom: 3px solid #2e2e2e;
  }
</style>

<nav id="navbar">
  <div class="navbarLeft">
    <div class="top">
      <div class="topLinks">
        <a href="#" class="topLink">Log In</a>
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
