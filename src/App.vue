<template>
  <div id="app">
    <div id="nav">
      <div class="nav--logo">
        <p class="name">
          Blog with <br> Animations example
        </p>
      </div>
      <div>
        <input type="checkbox" id="click">
      <label for="click" class="menu-btn">
        <i class="fas fa-bars"></i>
      </label>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
        <li class="design"><p>Design by <a href="https://www.linkedin.com/in/loyolajuan/" taget="_blank">Juan Loyola </a></p></li>
      </ul>
      </div>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  font-family: 'Poppins';
  color: #333;
}

#nav {
  display: flex;
  height: 80px;
  width: 100%;
  background: rgb(78, 147, 216);
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  z-index: 2;

  font-family: 'Poppins';
  color:#fff;
  position: sticky;
  top: 0;

  .name {
    font-family: 'poppins';
    font-size: 0.9rem;
    padding: 10px;
  }

  a {
    color: #fff;
    text-decoration: none;
    font-weight: bold;
    margin:10px;
    padding: 10px 10px;
  }
  a:hover {
    color:#d63434;
  }
}
#nav ul{
    display: flex;
    flex-wrap: wrap;
    list-style: none;
  }
  #nav ul li{
    margin: 0 3px;
  }
  #nav ul li a{
    color: #f2f2f2;
    text-decoration: none;
    font-size: 1rem;
    font-weight: 500;
    padding: 8px 1rem;
    border-radius: 5px;
    letter-spacing: 1px;
    transition: all 0.3s ease;
  }
  #nav ul li a:hover{
    color:#aeafb6;
  }
  #nav .menu-btn i{
    color: #fff;
    font-size: 22px;
    padding: 0 30px;
    cursor: pointer;
    display: none;
  }

  #nav .design{
    display:none;
  }

  input[type="checkbox"] {
    display: none;
  }
  @media (max-width: 1000px){
    #nav{
      padding: 0 40px 0 50px;
    }
  }
  @media (max-width: 920px) {
    #nav .menu-btn i{
      display: block;
    }
    #nav .design{
    display:block;
    a{
      color: rgb(98, 119, 211);
    }
  }
    #click:checked ~ .menu-btn i:before{
      content: "\f00d";
    }
    #nav ul{
      position: fixed;
      top: 80px;
      left: -100%;
      background: #111;
      height: 100vh;
      width: 100%;
      text-align: center;
      display: block;
      transition: all 0.3s ease;
    }
    #click:checked ~ ul{
      left: 0;
    }
    #nav ul li{
      width: 100%;
      margin: 40px 0;
    }
    #nav ul li a{
      width: 100%;
      margin-left: -100%;
      display: block;
      font-size: 20px;
      transition: 0.6s cubic-bezier(0.68, -0.55, 0.265, 1.55);
    }
    #click:checked ~ ul li a{
      margin-left: 0px;
    }
    #nav ul li a.active,
    #nav ul li a:hover{
      background: none;
      color: cyan;
    }
  }
  @media screen and (min-width: 320px) and (max-width:1034px){
    #nav{
      padding: 0px 0px;
      display:flex;
      width:100%;

      .name{
        font-size: 0.8rem;
      }
      .title{
        font-size: 0.6rem;
      }

      a{
        font-size: 0.6rem;
        display:flex;
        flex-direction: row wrap;
      }
    }
  }
</style>
