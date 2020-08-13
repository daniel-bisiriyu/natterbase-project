<template>
  <div class="layout-container">
    <!-- <div class="sidebar"> -->
    <app-sidebar />
    <!-- </div> -->
    <div class="content">
      <div class="navbar">
        <app-navbar />
      </div>
      <div class="main">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
import AppNavbar from "./partials/navbar";
import AppSidebar from "./partials/sidebar";
export default {
  components: {
    AppNavbar,
    AppSidebar,
  },
};
</script>

<style scoped>
.layout-container {
  display: flex;
}
.content {
  background: rgba(45, 45, 45, 0.04);
  width: 93%;
  margin-left: 7%;
  /* overflow: auto; */
}
/* .navbar {
  position: fixed;
  width: 98%;
}
.main {
  margin: 7rem 5rem 2rem;
} */
.main {
  margin: 2rem 5rem;
}
</style>
