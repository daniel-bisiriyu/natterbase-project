<template>
  <div class="modules">
    <div class="backlog">
      <Backlog />
    </div>
    <div class="todo">
      <Todo />
    </div>
    <div class="in-progress">
      <in-progress />
    </div>
    <div class="in-review">
      <in-review />
    </div>
    <div class="done">
      <Done />
    </div>
  </div>
</template>

<script>
import Backlog from "./backlog";
import Todo from "./todo";
import InProgress from "./InProgress";
import InReview from "./InReview";
import Done from "./done";
export default {
  components: {
    Backlog,
    Todo,
    InProgress,
    InReview,
    Done,
  },
};
</script>

<style scoped>
.modules {
  display: flex;
  margin-top: 1rem;
}
.modules > div {
  width: 20%;
  margin: 0 0.5rem;
}
.modules > div:first-of-type {
  margin-left: 0;
}
.modules > div:last-of-type {
  margin-right: 0;
}
</style>
