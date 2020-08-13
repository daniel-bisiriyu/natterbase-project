<template>
  <div class>
    <default-layout>
      <home-content />
    </default-layout>
  </div>
</template>

<script>
import DefaultLayout from "@/layouts/default";
import HomeContent from "./main";
export default {
  components: {
    DefaultLayout,
    HomeContent,
  },
};
</script>

<style>
</style>