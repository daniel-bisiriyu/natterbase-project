<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>-->
    <router-view />
  </div>
</template>

<style>
@font-face {
  font-family: "Nunito sans";
  src: url("./assets/NunitoSans-Regular.ttf");
  font-display: block;
}
* {
  font-family: "Nunito sans" !important;
}
body {
  padding: 0;
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.shadow {
  box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15) !important;
}
.heading {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
.el-switch__label.is-active {
  font-weight: bolder;
}
.el-switch__label--right {
  font-weight: bolder !important;
  color: #f15832 !important;
}
</style>
