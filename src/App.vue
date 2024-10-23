<template>
  <div id="app" style="display: flex; justify-content: space-between; align-content: center;">
    <img alt="Vue logo" src="./assets/logo.png" class="headerLogo">
    <div style="display: flex; justify-content: center;">
    <input type="text" placeholder="Search . . ." class="searchInput"><img alt="Search icon" src="./assets/search-icon.svg" style="max-width: 24px;max-height: 24px;">
    </div>
    <HamburgerMenu/>
  </div>
  <!-- <router-view/> -->
</template>

<script>
import HamburgerMenu from './components/HamburgerMenu.vue';
``
export default {
  components: {
    HamburgerMenu,
  },
};
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    /* margin-top: 60px; */
  }
 .headerLogo {
  max-width: 15%;
  max-height: 15%;
 }
.searchInput {
    border: none;
    background-color: transparent;
    font-size: 18;
    color: black;
    max-width: 165px;
    max-height: 32px
}
</style>
