<template>
  <div class="tests">
    <div class="modules">
      <Modules />
    </div>
    <div class="test-case">
      <added-test-case />
    </div>
    <div class="overview">
      <quick-overview />
    </div>
  </div>
</template>

<script>
import Modules from "./modules";
import AddedTestCase from "./AddedTestCase";
import QuickOverview from "./QuickOverview";

export default {
  components: {
    Modules,
    AddedTestCase,
    QuickOverview,
  },
};
</script>

<style scoped>
.tests {
  display: flex;
  margin-top: 1rem;
}
.modules {
  width: 25%;
  margin: 0 0.5rem 0 0;
}
.test-case {
  width: 40%;
  margin: 0 0.5rem;
}
.overview {
  width: 35%;
  margin: 0 0 0 1.5rem;
  border-radius: 0.5rem;
}
</style>
