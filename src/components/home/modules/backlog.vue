<template>
  <div class="backlog">
    <div class="heading">
      <p>Backlog</p>
      <div class="ellipsis">
        <svg
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g opacity="0.8">
            <path
              d="M13 12C13 11.4477 12.5523 11 12 11C11.4477 11 11 11.4477 11 12C11 12.5523 11.4477 13 12 13C12.5523 13 13 12.5523 13 12Z"
              stroke="#03293D"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              d="M6 12C6 11.4477 5.55228 11 5 11C4.44772 11 4 11.4477 4 12C4 12.5523 4.44772 13 5 13C5.55228 13 6 12.5523 6 12Z"
              stroke="#03293D"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              d="M20 12C20 11.4477 19.5523 11 19 11C18.4477 11 18 11.4477 18 12C18 12.5523 18.4477 13 19 13C19.5523 13 20 12.5523 20 12Z"
              stroke="#03293D"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </g>
        </svg>
      </div>
    </div>
    <div class="add-new-backlog" @click="addNewBacklogItem">
      <div class="plus-icon">
        <svg
          width="10"
          height="10"
          viewBox="0 0 10 10"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M9 5.14286H5.14286V9H3.85714V5.14286H0V3.85714H3.85714V0H5.14286V3.85714H9V5.14286Z"
            fill="#23B3E8"
          />
        </svg>
      </div>
    </div>

    <div class="new-item-input-area">
      <textarea
        type="text"
        placeholder="Add a new backlog"
        v-model="newBacklogItem"
        autofocus
      />
    </div>

    <div class="backlog-items">
      <backlog-item :items="backlogItems" />
    </div>
    <success :display="successfullyAddedItem" />
  </div>
</template>

<script>
import success from "../../success";
import BacklogItem from "./SingleBacklogItem";
export default {
  components: {
    BacklogItem,
    success,
  },
  data() {
    return {
      newBacklogItem: "",
      backlogItems: ["Apply gredient colours on the dashboard sidenav"],
      successfullyAddedItem: false,
    };
  },
  // watch: {
  //   newBacklogItem() {

  //   }
  // },
  mounted() {
    if (localStorage.backlogs) {
      this.backlogItems = JSON.parse(localStorage.getItem("backlogs"));
    } else {
      localStorage.setItem("backlogs", JSON.stringify(this.backlogItems));
    }
  },
  methods: {
    addNewBacklogItem() {
      console.log(localStorage.backlogs);
      var backlog = JSON.parse(localStorage.getItem("backlogs"));
      backlog.unshift(this.newBacklogItem);
      localStorage.setItem("backlogs", JSON.stringify(backlog));
      this.backlogItems = JSON.parse(localStorage.getItem("backlogs"));
      this.newBacklogItem = "";
      this.successfullyAddedItem = true;
      setTimeout(() => {
        this.successfullyAddedItem = false;
      }, 2000);
    },
  },
};
</script>

<style scoped>
.add-new-backlog {
  cursor: pointer;
  background: #ffffff;
  height: 2.5rem;
  width: 100%;
  border-radius: 0.25rem;
}
.heading {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.heading p {
  text-align: left;
  font-size: 0.9rem;
  font-weight: bolder;
}
.plus-icon {
  display: flex;
  justify-content: center;
  height: 100%;
  align-items: center;
}
.new-item-input-area {
  background: #ffffff;
  height: 4rem;
  width: 100%;
  margin-top: 1rem;
  border-radius: 0.25rem;
}
.new-item-input-area textarea {
  border: none;
  color: #03293d;
  padding-top: 0.75rem;
  font-size: 0.7rem;
  width: 90%;
}
.new-item-input-area textarea:focus {
  outline: none;
}
.backlog-items {
  margin-top: 1rem;
  border-radius: 0.5rem;
  width: 100%;
}
</style>
