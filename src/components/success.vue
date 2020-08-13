<template>
  <div class="success" v-if="display">
    <h5 class="text-center text-white">
      Modules have been created sucessfully
    </h5>
  </div>
</template>
<script>
export default {
  props: ["display"],
};
</script>
<style scoped>
.success {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 4rem;
  background-color: #4dbd98;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
