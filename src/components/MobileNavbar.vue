<template>
  <div class="mobile-navbar">
    <div class="mobile-navbar-left">
      <div class="mobile-navbar-item">Icon</div>
      <div class="mobile-navbar-item">Lang</div>
    </div>
    <div></div>
    <div class="mobile-navbar-right">
      <div class="mobile-navbar-item">Menu 3</div>
    </div>
  </div>
</template>

<style lang="less">
.mobile-navbar {
  display: grid;
  grid-template-columns: 25% auto 20%;

  @media (min-width: 700px) {
    display: none;
  }
}

.mobile-navbar-left {
  display: grid;
  background-color: cyan;
  grid-template-columns: 75px 75px;
  justify-content: center;
}

.mobile-navbar-right {
  background-color: black;
  display: grid;
  //grid-template-columns: 75px;
}

.mobile-navbar-item {
  background-color: yellowgreen;
  margin: 0.5em;
  padding: 0.5em;
  text-align: center;
}
</style>
