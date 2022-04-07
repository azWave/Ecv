<template>
  <div id="container">
    <header>
      <div>
        <nuxt-link  class="button" to="/">Accueil</nuxt-link>
        <nuxt-link class="button" to="/experience">Experiences</nuxt-link>
        <nuxt-link class="button" to="/projets">Projets</nuxt-link>
        <nuxt-link class="button" to="/contact">Contact</nuxt-link>
      </div>
    </header>
    <Nuxt />
    <footer>
      <div>
        <h1>Me contacter</h1>
        <a href="https://github.com/maximebourre" ><img src="../static/icon/Github_black.svg" alt="github" class="icon"></a>
        <a href="mailto:bourre.maxime.62@gmail.com" ><img src="../static/icon/Mail_black.svg" alt="mail" class="icon"></a>
        <a href="https://www.linkedin.com/in/maxime-bourre-1446b4211/" ><img src="../static/icon/LinkedIN_black.svg" alt="linkedin" class="icon"></a>
      </div>
    </footer>
  </div>
</template>


<style>
  @import url('https://fonts.googleapis.com/css2?family=Ubuntu+Mono');
  body{
    background-color: #393939;
    font-family: 'Ubuntu Mono';
    color: white;
    margin: 0;
    padding:0;
    font-size:20px;
  }
  header{
    font-size: 20px;
    height: 50px;
    padding-top: 10px;
    text-align: center;
    display: block;
  }
  header div{
    margin: auto;
  }
  header a{
    display:block;
    float:left;   
    color:#73A1F8;
    text-transform: uppercase;
    margin-left: 2%;
    margin-right: 2%;
    text-decoration-line: none;
    font-weight: bold;
  }
  footer{
    margin: 0;
    width: 100%;

  }
  footer div{
    margin: 0;
    width: 100%;
    text-align: center;
    background-color: #73A1F8;
    height: 150px;
  }
  footer h1{
    padding-top: 0px;
    margin-top: 0%;
  }
  footer a {
    margin-left: 10%;
    margin-right: 10%;
    padding-top: 15px;
  }
  
  .content{
    padding-right: 12%;
    padding-left: 12%;
    height: 105vh ;
    z-index: -2;
  }

  .content .text{
    width: 50%;
    margin-right: 0;
  }
  .content .image{
    text-align: center;
    justify-content: center;
  }
  img{
    width:100%;
  }
  .icon{
    width: 48px ;
  }
  .inline{
    margin: 0;
    padding: 0;
    display: inline;
  }
  .dark{
  background-color: #303030;
  }
  .content h1{
    padding-top: 3%;
    text-align: center;
    color: #73A1F8;
    margin-bottom: 10%;
  }
  .color{
    color: #73A1F8;
  }

</style>
