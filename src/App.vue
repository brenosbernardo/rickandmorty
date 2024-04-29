<script setup>
import {ref} from 'vue'
</script>

<template>
  <nav class="navbar">
  <div class="container-fluid">
    <!-- <a class="navbar-brand" href="#">Rick and Morty</a> -->
    <img src="https://www.icegif.com/wp-content/uploads/2022/06/icegif-519.gif" height="100" width="100" alt="Logo" class="navbar-logo">
    <router-link class="navbar-brand" to="/">Rick and Morty</router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <!-- <a class="nav-link active" aria-current="page" href="#">Início</a> -->
          <router-link class="nav-link" aria-current="page" to="/">Inicio</router-link>
        </li>
        <li class="nav-item">
          <!-- <a class="nav-link" href="#">Sobre</a> -->
          <router-link class="nav-link" to="/about">Sobre</router-link>
        </li>
      </ul>
    </div>
  </div>
</nav>

<div class="main">
  <router-view></router-view>
</div>

<footer class="footer text-light">
  <div class="a">
    &copy; Breno Silva Bernardo {{ new Date().getFullYear() }}
  </div>
</footer>
</template>
<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap');
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

.section{
  width: 100%;
  justify-content: center;
  position: relative;
}

.template{
  align-items: center;
}


.navbar-logo{
  float: right;
}

.carde {
    border: none;
    float: left;
    text-align: center;
}
.cardi{
  width: 200%;
  text-align: center;
  align-items: center;
  border: none;
  float: left;
}

.card {
    border: none;
    float: left;
    text-align: center
}

.card-text {
    background-size: 550px 60px; 
    align-items: center;
    background-repeat: no-repeat; 
    color: transparent;
    text-align: center; 
}


.navbar-brand{
  color: #FFFFFF;
  text-align: center;
  align-items: center;
}
.nav-link{
  color: #FFFFFF;
  text-align: center;
  align-items: center;
}
.navbar{
  background-color:#252222;
  align-items: center;
  border-radius: 2px;
}

.navbar-toggler{
  background-color:#577c4c;
}

.texto {
  position: absolute;
  top: 250px;
  right: 20px; 
  width: 600px; 
  text-align: right; 
}

.texto h1{
  font-size: 20px;
}


footer{
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 50px;
  background-color: #252222;
}

body{
  background-color: #577c4c;
}


</style>

