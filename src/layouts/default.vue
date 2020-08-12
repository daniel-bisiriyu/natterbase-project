<template>
  <div class="layout-container">
    <app-sidebar />
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
  background: #e5e5e5;
  width: 93%;
  /* margin-left: 7%; */
}
</style>