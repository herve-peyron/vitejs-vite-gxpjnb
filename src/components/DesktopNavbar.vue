<script setup>
import MenuX from './Menu.vue';
import DropdownItem from './DropdownItem.vue';
</script>

<template>
  <div class="desktop-navbar">
    <div class="desktop-navbar-left">
      <div class="desktop-navbar-item">Icon</div>
      <div class="desktop-navbar-item">Lang</div>
    </div>
    <div class="desktop-navbar-center">
      <dropdown-item title="Menu 1">
        <h1>Choix 1</h1>
        <h1>Choix 2</h1>
      </dropdown-item>
      <dropdown-item title="Menu 2">
        <div class="menu2-class">
          <h1>Choix 3</h1>
          <h1>Choix 4</h1>
        </div>
      </dropdown-item>
      <div class="desktop-navbar-item">Menu 2</div>
    </div>
    <div class="desktop-navbar-right">
      <div class="desktop-navbar-item">Menu 3</div>
    </div>
  </div>
  <!-- <menu-x v-if="hover"></menu-x -->
</template>

<script>
export default {
  data() {
    return {
      hover: false,
    };
  },
};
</script>

<style lang="less">
.desktop-navbar {
  display: grid;
  grid-template-columns: 25% auto 20%;

  @media (max-width: 700px) {
    display: none;
  }

  .desktop-navbar-left {
    display: grid;
    background-color: cyan;
    grid-template-columns: 75px 75px;
    justify-content: center;
  }

  .desktop-navbar-center {
    display: grid;
    background-color: red;
    grid-template-columns: 90px 90px 90px;
    justify-content: space-evenly;
    margin: 0.5em;
    padding: 0.5em;

    .menu2-class {
      background-color: white;
      padding: 1em;
    }
  }

  .desktop-navbar-right {
    background-color: black;
    display: grid;
    //grid-template-columns: 75px;
  }
}

.desktop-navbar-item {
  background-color: yellowgreen;
  text-align: center;
  //margin: 0.5em;
  padding: 0.5em;
  &:hover {
    background-color: lighten(yellowgreen, 20%);
  }
}
</style>
