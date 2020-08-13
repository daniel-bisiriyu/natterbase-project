<template>
  <div class="navigation-tab">
    <div class="nav-items">
      <div :class="{'active': onOverviewTab}" class="nav-item" @click="changeTab('overview')">
        <p>Overview</p>
      </div>
      <div :class="{'active': onTeamsTab}" class="nav-item" @click="changeTab('teams')">
        <p>Teams</p>
      </div>
      <div :class="{'active': onModulesTab}" class="nav-item" @click="changeTab('modules')">
        <p>Modules</p>
      </div>
      <div :class="{'active': onTestTab}" class="nav-item" @click="changeTab('tests')">
        <p>Tests</p>
      </div>
      <div :class="{'active': onFilesTab}" class="nav-item" @click="changeTab('files')">
        <p>Files</p>
      </div>
      <div :class="{'active': onProgressTab}" class="nav-item" @click="changeTab('progress')">
        <p>Progress</p>
      </div>
    </div>
    <div class="tab-meta">
      <div class="toggle-control-area">
        <el-switch
          style="display: block"
          v-model="switchValue"
          active-color="#13ce66"
          inactive-color="#f15832"
          active-text="All Modules"
          inactive-text="All Task"
        ></el-switch>
      </div>
      <div class="project-deadline">
        <div class="calendar-icon">
          <svg
            width="16"
            height="16"
            viewBox="0 0 16 16"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M11.75 2.25H14.75C14.9489 2.25 15.1397 2.32902 15.2803 2.46967C15.421 2.61032 15.5 2.80109 15.5 3V15C15.5 15.1989 15.421 15.3897 15.2803 15.5303C15.1397 15.671 14.9489 15.75 14.75 15.75H1.25C1.05109 15.75 0.860322 15.671 0.71967 15.5303C0.579018 15.3897 0.5 15.1989 0.5 15V3C0.5 2.80109 0.579018 2.61032 0.71967 2.46967C0.860322 2.32902 1.05109 2.25 1.25 2.25H4.25V0.75H5.75V2.25H10.25V0.75H11.75V2.25ZM14 8.25H2V14.25H14V8.25ZM10.25 3.75H5.75V5.25H4.25V3.75H2V6.75H14V3.75H11.75V5.25H10.25V3.75ZM3.5 9.75H5V11.25H3.5V9.75ZM7.25 9.75H8.75V11.25H7.25V9.75ZM11 9.75H12.5V11.25H11V9.75Z"
              fill="#4DBD98"
            />
            <path
              d="M11.75 2.25H14.75C14.9489 2.25 15.1397 2.32902 15.2803 2.46967C15.421 2.61032 15.5 2.80109 15.5 3V15C15.5 15.1989 15.421 15.3897 15.2803 15.5303C15.1397 15.671 14.9489 15.75 14.75 15.75H1.25C1.05109 15.75 0.860322 15.671 0.71967 15.5303C0.579018 15.3897 0.5 15.1989 0.5 15V3C0.5 2.80109 0.579018 2.61032 0.71967 2.46967C0.860322 2.32902 1.05109 2.25 1.25 2.25H4.25V0.75H5.75V2.25H10.25V0.75H11.75V2.25ZM14 8.25H2V14.25H14V8.25ZM10.25 3.75H5.75V5.25H4.25V3.75H2V6.75H14V3.75H11.75V5.25H10.25V3.75ZM3.5 9.75H5V11.25H3.5V9.75ZM7.25 9.75H8.75V11.25H7.25V9.75ZM11 9.75H12.5V11.25H11V9.75Z"
              fill="#4DBD98"
            />
            <path
              d="M11.75 2.25H14.75C14.9489 2.25 15.1397 2.32902 15.2803 2.46967C15.421 2.61032 15.5 2.80109 15.5 3V15C15.5 15.1989 15.421 15.3897 15.2803 15.5303C15.1397 15.671 14.9489 15.75 14.75 15.75H1.25C1.05109 15.75 0.860322 15.671 0.71967 15.5303C0.579018 15.3897 0.5 15.1989 0.5 15V3C0.5 2.80109 0.579018 2.61032 0.71967 2.46967C0.860322 2.32902 1.05109 2.25 1.25 2.25H4.25V0.75H5.75V2.25H10.25V0.75H11.75V2.25ZM14 8.25H2V14.25H14V8.25ZM10.25 3.75H5.75V5.25H4.25V3.75H2V6.75H14V3.75H11.75V5.25H10.25V3.75ZM3.5 9.75H5V11.25H3.5V9.75ZM7.25 9.75H8.75V11.25H7.25V9.75ZM11 9.75H12.5V11.25H11V9.75Z"
              fill="#4DBD98"
            />
            <path
              d="M11.75 2.25H14.75C14.9489 2.25 15.1397 2.32902 15.2803 2.46967C15.421 2.61032 15.5 2.80109 15.5 3V15C15.5 15.1989 15.421 15.3897 15.2803 15.5303C15.1397 15.671 14.9489 15.75 14.75 15.75H1.25C1.05109 15.75 0.860322 15.671 0.71967 15.5303C0.579018 15.3897 0.5 15.1989 0.5 15V3C0.5 2.80109 0.579018 2.61032 0.71967 2.46967C0.860322 2.32902 1.05109 2.25 1.25 2.25H4.25V0.75H5.75V2.25H10.25V0.75H11.75V2.25ZM14 8.25H2V14.25H14V8.25ZM10.25 3.75H5.75V5.25H4.25V3.75H2V6.75H14V3.75H11.75V5.25H10.25V3.75ZM3.5 9.75H5V11.25H3.5V9.75ZM7.25 9.75H8.75V11.25H7.25V9.75ZM11 9.75H12.5V11.25H11V9.75Z"
              fill="#4DBD98"
            />
          </svg>
        </div>
        <div class="deadline-text">
          <p>Project Deadline: 6 Weeks</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      switchValue: false,
      onOverviewTab: false,
      onTeamsTab: false,
      onModulesTab: true,
      onTestTab: false,
      onFilesTab: false,
      onProgressTab: false,
    };
  },
  methods: {
    changeTab(newTab) {
      this.$emit("changeTab", newTab);
      if (newTab == "tests") {
        this.onTestTab = true;
        this.onModulesTab = false;
        console.log("modules tab " + this.onModulesTab);
      } else if (newTab == "modules") {
        this.onModulesTab = true;
        this.onTestTab = false;
        console.log("test tab " + this.onTestTab);
      }
    },
  },
};
</script>

<style scoped>
.navigation-tab {
  display: flex;
  /* opacity: 0.2; */
  border-bottom: 1px solid #d1d1d1;
}
.nav-items {
  display: flex;
  width: 50%;
}
.nav-item {
  padding: 0 1.25rem;
  color: #859aa5;
  cursor: pointer;
}
.nav-item:first-of-type {
  padding: 0 1.25rem 0 0;
}
.nav-item p {
  font-size: 0.9rem;
  margin-bottom: 0.6rem;
  font-weight: bolder;
  text-align: center;
}
.nav-item p:first-of-type {
  text-align: left;
}
.nav-item.active {
  color: #f15832;
  border-bottom: 1.5px solid #f15832;
}
.tab-meta {
  width: 50%;
  display: flex;
  justify-content: flex-end;
  align-items: center;
}
.project-deadline {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 1rem;
}
.deadline-text p {
  color: #4dbd98;
  font-size: 0.8rem;
  font-weight: bolder;
  margin-left: 0.5rem;
}
.toggle-control-area {
  margin-right: 5rem;
}
</style>
