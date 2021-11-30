<template>
  <div class="d1"></div>
</template>

<style lang="less">
div {
  width: 90%;
  height: 200px;
  margin: 0 auto 20px auto;
  border: 2px solid black;
  box-sizing: border-box;
}
.d1 {
  background-color: orange;
  animation-name: couleur;
  animation-duration: 4s;
}
@keyframes couleur {
  from {
    background-color: orange;
  }
  to {
    background-color: blue;
  }
}
</style>
