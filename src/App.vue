<template>
  <Modal v-bind:isModal="isModal" />
  <Menu />
  <Sales />
</template>

<script>
import Sales from "./components/Sales.vue";
import Menu from "./components/Menu.vue";
import Modal from "./components/Modal.vue";
export default {
  name: "App",
  components: {
    Sales,
    Menu,
    Modal,
  },
  data() {
    return {
      isModal: false,
    };
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
