<template>
  <div>
    <div class="context">
      <h1 class="title">We are</h1>
      <h1 class="title">Moffhub Solutions</h1>
      <h2 class="subtitle">The Future Now</h2>
      <img class="image" src="/imgs/mlogo.png"/>
    </div>
    <div class="area" >
      <ul class="circles">
        <li/>
        <li/>
        <li/>
        <li/>
        <li/>
        <li/>
        <li/>
        <li/>
        <li/>
        <li/>
      </ul>
    </div >
    <section class="intro hero is-medium has-text-centered" id="hero">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">
            Welcome to
            <br/>
            MoffHub Solutions
          </h1>
          <br/>
          <h2 class="subtitle">We are a Software design and development and IOT Company based in Nairobi, Kenya.</h2>
          <br/>
          <h2 class="subtitle">We are passionate about Websites and Hardware concepts, integrating hardware and software
            interfaces, PCB Designs to High Quality and Custom Web apps.</h2>
          <br/>
          <h2 class="subtitle">We are bringing the future to the present.</h2>
        </div>
      </div>
    </section>
  </div>

</template>
<style scoped>
  @import url('https://fonts.googleapis.com/css?family=Exo:400,700');

  *{
    margin: 0px;
    padding: 0px;
  }

  body{
    font-family: 'Exo', sans-serif;
  }

  .image {
    margin: 0 auto;
    height: 20vh
  ;
  }
  .context {
    width: 100%;
    position: absolute;
    top:30vh;

  }

  .context h1{
    text-align: center;
    color: #fff;
    font-size: 50px;
  }
  .context h2 {
    text-align:center;
    color: #fff;
  }
  .area{
    background: #375980;
    /*background: -webkit-linear-gradient(to left, #1cfbab, #3dc812);*/
    width: 100%;
    height:100vh;
  }

  .circles{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
  }

  .circles li{
    position: absolute;
    display: block;
    list-style: none;
    width: 20px;
    height: 20px;
    background: rgba(255, 255, 255, 0.2);
    animation: animate 25s linear infinite;
    bottom: -150px;

  }

  .circles li:nth-child(1){
    left: 25%;
    width: 80px;
    height: 80px;
    animation-delay: 0s;
  }


  .circles li:nth-child(2){
    left: 10%;
    width: 20px;
    height: 20px;
    animation-delay: 2s;
    animation-duration: 12s;
  }

  .circles li:nth-child(3){
    left: 70%;
    width: 20px;
    height: 20px;
    animation-delay: 4s;
  }

  .circles li:nth-child(4){
    left: 40%;
    width: 60px;
    height: 60px;
    animation-delay: 0s;
    animation-duration: 18s;
  }

  .circles li:nth-child(5){
    left: 65%;
    width: 20px;
    height: 20px;
    animation-delay: 0s;
  }

  .circles li:nth-child(6){
    left: 75%;
    width: 110px;
    height: 110px;
    animation-delay: 3s;
  }

  .circles li:nth-child(7){
    left: 35%;
    width: 150px;
    height: 150px;
    animation-delay: 7s;
  }

  .circles li:nth-child(8){
    left: 50%;
    width: 25px;
    height: 25px;
    animation-delay: 15s;
    animation-duration: 45s;
  }

  .circles li:nth-child(9){
    left: 20%;
    width: 15px;
    height: 15px;
    animation-delay: 2s;
    animation-duration: 35s;
  }

  .circles li:nth-child(10){
    left: 85%;
    width: 150px;
    height: 150px;
    animation-delay: 0s;
    animation-duration: 11s;
  }



  @keyframes animate {

    0%{
      transform: translateY(0) rotate(0deg);
      opacity: 1;
      border-radius: 0;
    }

    100%{
      transform: translateY(-1000px) rotate(720deg);
      opacity: 0;
      border-radius: 50%;
    }

  }
  .intro {
    background-color: #4d5450;
    color: white;
    background: -webkit-linear-gradient(to right, #2ad382, #4d5450);
    background:    -moz-linear-gradient(to right, #2ad382, #4d5450);
    background:         linear-gradient(to right, #2ad382, #4d5450);
  }
  .intro h1 {
    color: white;
  }
  .intro h2 {
    color:white;
  }
</style>
