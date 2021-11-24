<template>
  <div class="dropdown-container">
    <button @onclick="click()">{{ title }}</button>
    <div class="dropdown-content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: ['title'],
  methods: {
    click() {
      console.log('Click :-)');
    },
  },
};
</script>

<style lang="less">
.dropdown-container {
  display: flex;
  //justify-content: center;
  align-items: center;
  flex-direction: column;
  //position: relative;

  &:hover .dropdown-content {
    display: grid;
  }

  button {
    border: none;
    background: lighten(red, 30%);
    //border: 3px solid yellow;
    &:hover {
      background-color: #234567;
    }
  }

  .dropdown-content {
    display: none;
    position: absolute;
    //justify-content: space-between;
    margin-top: 2em;
    z-index: 1;
    //background-color: white;
    //height: 400px;
    //width: 400px;
    box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);

    &:hover {
      background-color: #111ddd;
    }
  }
}
</style>
