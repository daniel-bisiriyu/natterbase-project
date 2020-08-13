<template>
  <div class="test-cases-container">
    <div class="tests">
      <div
        class="single-test-case"
        v-for="testCase in testCases"
        :key="testCase.id"
      >
        <div>
          <p>{{ testCase.name }}</p>
        </div>
        <div class="action-button" @click="shouldShowPopup(testCase.id)">
          <p>
            {{ testCase.status }}
            <span>
              <svg
                width="10"
                height="7"
                viewBox="0 0 10 7"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M1.44678 1.625L5.19678 5.375L8.94678 1.625"
                  stroke="#ffffff"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </span>
          </p>
        </div>
        <div class="test-case--popup shadow" v-if="selectedId == testCase.id">
          <div class="popup-input-container">
            <input type="text" placeholder="Search" class="popup-input" />
          </div>
          <div class="popup-options">
            <li @click="changeStatus('Pass')">Pass</li>
            <li @click="changeStatus('Failed')">Failed</li>
            <li @click="changeStatus('Retest')">Retest</li>
            <li @click="changeStatus('Untest')">Untest</li>
          </div>
        </div>
      </div>
    </div>
    <div class="action-buttons">
      <button class="new-test-case">New Test Case</button>
      <button class="test">Test</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showPopup: false,
      selectedId: null,
      testCases: [
        {
          name: "Make the background image blur",
          status: "Pass",
          id: 1,
        },
        {
          name: "Apply gredient colours on the navigation",
          status: "Pass",
          id: 2,
        },
        {
          name: "Make the background image blur",
          status: "Pass",
          id: 3,
        },
        {
          name: "Apply gredient colours on the navigation",
          status: "Pass",
          id: 4,
        },
      ],
    };
  },
  methods: {
    shouldShowPopup(id) {
      if (this.selectedId) {
        this.selectedId = null;
      } else {
        this.selectedId = id;
      }
    },
    changeStatus(val) {
      if (val == "Pass") {
        var testCaseToUpdate = this.testCases.filter((testcase) => {
          return testcase.id == this.selectedId;
        });
        testCaseToUpdate[0].status = "Pass";
      }
    },
  },
};
</script>

<style scoped>
.test-cases-container {
  background: #ffffff;
  width: 100%;
  padding: 1rem 1rem 1rem 0;
  overflow: auto;
}
.test-cases-container::-webkit-scrollbar {
  width: 4px !important;
}
.test-cases-container::-webkit-scrollbar-track {
  box-shadow: inset 0 0 5px #d3d3d3;
  border-radius: 10px;
}
.test-cases-container::-webkit-scrollbar-thumb {
  background: #c0c0c0;
  border-radius: 10px;
}

.single-test-case p {
  color: #03293d;
  margin: 0;
  font-weight: 600;
}
.single-test-case {
  position: relative;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-left: 0;
  padding: 2rem 0.5rem 0.25rem 1rem;
}
.test-cases-container > div:first-of-type > div:first-of-type {
  padding: 0.25rem 0.5rem 0.25rem 1rem;
  border-left: 2px solid #f15832;
}
.single-test-case.active {
  border-left: 2px solid #f15832;
}
.action-button {
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 4rem;
  height: 1.8rem;
  background: linear-gradient(0deg, #4dbd98, #4dbd98),
    linear-gradient(0deg, #4dbd98, #4dbd98),
    linear-gradient(0deg, #4dbd98, #4dbd98), #4dbd98;
  border: 2px solid rgba(26, 12, 47, 0.1);
  border-radius: 0.25rem;
}
.action-button p {
  color: #ffffff;
  font-weight: normal;
  font-size: 0.9rem;
}
.test-case--popup {
  position: absolute;
  z-index: 1;
  background: #ffffff;
  width: 12rem;
  /* height: 8rem; */
  border-radius: 0.5rem;
  top: 2.4rem;
  right: 0;
}
.popup-input {
  border: none;
  background: #eeecf1;
  /* opacity: 0.06; */
  padding: 0 0.5rem;
  height: 2rem;
  border-radius: 5px;
  width: 80%;
  margin: 0.5rem auto;
}
.popup-input:focus {
  outline: none;
}
.popup-input-container input::placeholder {
  color: #03293d !important;
  opacity: 0.4;
}
.popup-options {
  padding-bottom: 1rem;
}
.popup-options li {
  cursor: pointer;
  font-size: 0.85rem;
  font-weight: bolder;
  list-style-type: none;
  color: #03293d;
  text-align: left;
  padding: 0.25rem 1rem;
}
.popup-options li:hover {
  background: #e8e7ea;
}
.action-buttons {
  display: flex;
  justify-content: space-between;
  margin-top: 1.5rem;
  margin: 2rem 1rem;
}
.new-test-case {
  cursor: pointer;
  width: 12rem;
  height: 3rem;
  color: #ffffff;
  background: #23b3e8;
  border: 2px solid rgba(26, 12, 47, 0.1);
  box-sizing: border-box;
  border-radius: 5px;
}
.test {
  cursor: pointer;
  width: 12rem;
  height: 3rem;
  background: #ffffff;
  border: 2px solid #03293d;
  box-sizing: border-box;
  border-radius: 5px;
}
</style>
