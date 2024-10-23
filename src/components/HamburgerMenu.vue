<template>
    <div>
      <div class="hamburger" @click="toggleMenu">
        <div class="bar" :class="{ 'open': isOpen }"></div>
        <div class="bar" :class="{ 'open': isOpen }"></div>
        <div class="bar" :class="{ 'open': isOpen }"></div>
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
        console.log(page)
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
    background-color: #42b883
  }
  
  .menu {
    background-color: #f8f9fa;
    position: absolute;
    top: 20px;
    right: 7%;
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
  </style>
  