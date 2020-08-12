<template>
  <div class="home">
    <!-- <sidebar /> -->
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <main-content />
  </div>
</template>

<script>
// @ is an alias to /src
import MainContent from "@/components/home/index";
// import sidebar from "@/layouts/partials/sidebar";

export default {
  name: "Home",
  components: {
    MainContent,
    // sidebar,
  },
};
</script>
