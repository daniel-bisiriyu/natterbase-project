<template>
  <div class="app-navbar">
    <div class="content">
      <nav-items />
    </div>
  </div>
</template>

<script>
import NavItems from "./NavbarItems";
export default {
  components: {
    NavItems,
  },
};
</script>

<style scoped>
.app-navbar {
  width: 100%;
  background: #fbfbfb;
  margin: 0;
  height: 5rem;
}
</style>