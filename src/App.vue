<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <header>
    

      <nav class=nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/register">Register</RouterLink>
        <RouterLink to="/log-in">LogIn</RouterLink>
        <RouterLink to="">help</RouterLink>
         <!-- <RouterLink to=`/cart/:${user}`>cart</RouterLink> -->
      </nav>

  </header>

  <RouterView />
</template>

<style scoped>
.router-link-exact-active{
  color:red;
  font-size:23px;
}
.nav{
  height: 60px;
  width:99vw;
  background-color:rgb(245, 161, 66);
  display:flex;
  justify-content:space-evenly;
  align-items:center;
}
a{
  text-decoration:none;
  color:black
}
nav{
  font-size:20px;
}
</style>
