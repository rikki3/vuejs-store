<template>
  <img alt="Vue logo" src="../assets/logo.png" class="headerLogo" />
  <div style="display: flex; justify-content: center;">
    <input type="text" placeholder="Search . . ." class="searchInput" />
    <img alt="Search icon" src="../assets/search-icon.svg" style="max-width: 24px; max-height: 24px;margin-top: 3%;" />
  </div>
  <div>
    <div class="hamburger" @click="toggleMenu">
      <div class="bar" :class="{ open: isOpen, rotateTop: isOpen }"></div>
      <div class="bar" :class="{ open: isOpen, hide: isOpen }"></div>
      <div class="bar" :class="{ open: isOpen, rotateBottom: isOpen }"></div>
    </div>
    <nav v-if="isOpen" class="menu">
      <ul>
        <li @click="navigateTo('home')">Home</li>
        <li @click="navigateTo('about')">About</li>
        <li @click="navigateTo('contact')">Contact</li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen;
    },
    navigateTo(page) {
      console.log(page);
    },
  },
};
</script>

<style scoped>
.hamburger {
  cursor: pointer;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  width: 40px;
  height: 40px;
}

.bar {
  height: 4px;
  width: 100%;
  background-color: #333;
  transition: 0.3s;
}

.open {
  background-color: #42b883;
}

.rotateTop {
  transform: rotate(45deg) translate(5px, 13.5px);
}

.rotateBottom {
  transform: rotate(-45deg) translate(5px, -13.5px);
}

.hide {
  opacity: 0;
  height: 0;
  padding: 0;
  margin: 0;
}

.menu {
  background-color: #f8f9fa;
  position: absolute;
  top: 20px;
  margin-top: 10%;
  right: 10%;
  border: 1px solid #ddd;
  border-radius: 5px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.menu ul {
  list-style: none;
  padding: 2px;
}

.menu li {
  padding: 10px 20px;
  cursor: pointer;
}

.menu li:hover {
  background-color: #e9ecef;
}

.headerLogo {
  max-width: 15%;
  max-height: 15%;
}

.searchInput {
  border: none;
  background-color: transparent;
  font-size: 18px;
  color: black;
  max-width: 165px;
  max-height: 16px;
  margin-top: 5%;
  accent-color: #42b883;
}
</style>
