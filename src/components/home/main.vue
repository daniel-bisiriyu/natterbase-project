<template>
  <div>
    <navigation-tab />
    <Modules />
  </div>
</template>

<script>
import NavigationTab from "./NavigationTab";
import Modules from "./modules/index";

export default {
  components: {
    NavigationTab,
    Modules,
  },
};
</script>

<style></style>
