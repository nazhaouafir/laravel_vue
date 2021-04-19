<template>
  <div id="app">
  <nav  class="nav justify-content-center">
    <router-link class="nav-link active" to="/">Home</router-link>
    <router-link class="nav-link" to="/login">Login</router-link>
    <router-link class="nav-link " to="/register">Register</router-link>
  </nav>
   
    <router-view/>
  </div>
</template>

<style scoped>
.nav-link{
  font-size: 20px;
  color: rgb(119, 38, 76);
}
.nav-link:hover{
  background-color: antiquewhite;
  color: rgb(53, 4, 4);
}



</style>
