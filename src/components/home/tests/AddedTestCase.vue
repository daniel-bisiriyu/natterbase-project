<template>
  <div class="added-test-case">
    <div class="heading">
      <p>Added Test Case</p>
    </div>
    <div class="test-cases">
      <test-cases />
    </div>
  </div>
</template>

<script>
import TestCases from "./TestCases";
export default {
  components: {
    TestCases,
  },
};
</script>

<style scoped>
.heading p {
  color: #03293d;
  font-weight: bolder;
  font-size: 1.1rem;
}
</style>