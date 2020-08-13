<template>
  <div class="single-backlog-item">
    <div class="backlog-item-row backlog-item--first-row">
      <div>
        <p>Apply gredient colours on the dashboard sidenav</p>
      </div>
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
    <div class="backlog-item-row backlog-item--second-row">
      <div>
        <div class="clock-icon">
          <svg
            width="11"
            height="11"
            viewBox="0 0 11 11"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M5.49983 0.458336C2.71534 0.458336 0.45816 2.71563 0.45816 5.5C0.45816 8.28449 2.71534 10.5417 5.49983 10.5417C8.28432 10.5417 10.5415 8.28449 10.5415 5.5C10.5415 2.71563 8.28432 0.458336 5.49983 0.458336ZM5.49983 9.625C3.22168 9.625 1.37483 7.77826 1.37483 5.5C1.37483 3.22186 3.22168 1.375 5.49983 1.375C7.77797 1.375 9.62483 3.22186 9.62483 5.5C9.62483 7.77826 7.77797 9.625 5.49983 9.625ZM7.19887 6.55096C7.37785 6.72994 7.37785 7.02018 7.19887 7.19916C7.10949 7.28853 6.99205 7.33334 6.87483 7.33334C6.75761 7.33345 6.64028 7.28865 6.55079 7.19916L5.17579 5.82416C5.08985 5.73822 5.04149 5.62169 5.04149 5.5V2.75C5.04149 2.49689 5.24671 2.29167 5.49983 2.29167C5.75294 2.29167 5.95816 2.49689 5.95816 2.75V5.31025L7.19887 6.55096Z"
              fill="#03293D"
            />
          </svg>
        </div>
        <div>
          <p class="due-date">Due Aug 8</p>
        </div>
      </div>
      <div class="user-list-images">
        <img src="@/assets/users-image-row.svg" alt="List of users" />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.single-backlog-item {
  width: 100%;
  height: 6rem;
  background: #ffffff;
  margin-top: 1rem;
}
.single-backlog-item:first-of-type {
  margin-top: 0;
}
.backlog-item-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.1rem 0.5rem;
}
.backlog-item-row p {
  font-size: 0.7rem;
  text-align: left;
  color: #03293d;
}
.backlog-item--second-row > div:first-of-type {
  display: flex;
  justify-content: flex-start;
  align-items: center;
}
small {
  text-align: left;
}
.due-date {
  padding-left: 0.5rem;
}
.backlog-item--second-row > div:first-of-type {
  color: #03293d;
  opacity: 0.5;
}
</style>