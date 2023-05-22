<template>
  <div class="sub-group" @click="onOpen()">
    <div class="placeholder">
      <a href="#">
        {{ title }}
      </a>
      <svg viewBox="0 0 1030 638" width="10">
        <path
          d="M1017 68L541 626q-11 12-26 12t-26-12L13 68Q-3 49 6 24.5T39 0h952q24 0 33 24.5t-7 43.5z"
          fill="#394867"
        ></path>
      </svg>
    </div>
    <div class="sub-menu" v-if="isOpen">
      <div
        v-for="(item, index) in items"
        :key="index"
        class="menu-item"
        @click="updateOption(item.title)"
      >
        <a :href="item.link">{{ item.title }}</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    };
  },
  props: ["title", "items"],
  methods: {
    onOpen() {
      this.isOpen = !this.isOpen;
    },
    updateOption(option) {
      this.$emit("optionSelected", option);
      // console.log(option)
    },
  },
};
</script>

<style>
.sub-group {
  background: #ffffff;
  border: 1px solid rgba(0, 0, 0, 0.36);
  border-radius: 30px;
  width: 300px;
  height: 60px;
  display: flex;
  align-items: center;
  cursor: pointer;
}

.sub-group a {
  color: var(--font-color);
  font-size: 20px;
  font-weight: 400;
  line-height: 23px;
  font-family: var(--font-style);
  text-decoration: none;
  padding: 0 16px;
}

.sub-group a:hover {
  text-decoration: none;
}

.placeholder {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.placeholder svg {
  margin-right: 16px;
  width: 20px;
  height: 20px;
}

.sub-menu {
  position: absolute;
  top: calc(50% + 45px);
  width: 300px;
}

.menu-item {
  border: 1px solid rgba(0, 0, 0, 0.36);
  border-radius: 10px;
  padding: 8px;
  background-color: #ffffff;
}

.menu-item:hover {
  background-color: #0d6efd;
  color: #fff;
}

.menu-item a {
  color: inherit;
}

</style>
