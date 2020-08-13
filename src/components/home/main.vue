<template>
  <div>
    <navigation-tab @changeTab="changeToNewTab" />
    <Modules v-if="modules" />
    <Tests v-if="tests" />
  </div>
</template>

<script>
import NavigationTab from "./NavigationTab";
import Modules from "./modules/index";
import Tests from "./tests/index";

export default {
  components: {
    NavigationTab,
    Modules,
    Tests,
  },
  data() {
    return {
      modules: true,
      tests: false,
    };
  },
  methods: {
    changeToNewTab(event) {
      if (event == "tests") {
        this.tests = true;
        this.modules = false;
      } else if (event == "modules") {
        this.modules = true;
        this.tests = false;
      }
    },
  },
};
</script>

<style></style>
