<template>
  <div class="home">
    <!-- <sidebar /> -->
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <HelloWorld />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/home/index";
// import sidebar from "@/layouts/partials/sidebar";

export default {
  name: "Home",
  components: {
    HelloWorld,
    // sidebar,
  },
};
</script>
