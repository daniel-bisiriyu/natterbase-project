<template>
  <div class="test-cases-container">
    <div class="tests" v-for="n in 3" :key="n">
      <div class="single-test-case first">
        <div>
          <p>Make the background image blur</p>
        </div>
        <div class="action-button">
          <p>
            Pass
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
      </div>
      <div class="single-test-case">
        <div>
          <p>Apply gredient colours on the navigation</p>
        </div>
        <div class="action-button">
          <p>
            Pass
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
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.test-cases-container {
  background: #ffffff;
  width: 100%;
  /* height: 20rem; */
  padding: 1rem 1rem 1rem 0;
}
.single-test-case p {
  color: #03293d;
  margin: 0;
  font-weight: 600;
}
.single-test-case {
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
</style>