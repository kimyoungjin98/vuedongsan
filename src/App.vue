<template>
  <Menu />
  <Sales v-bind:imgClick="imgClick" v-bind:isModal="isModal" />
  <div class="black-bg" v-if="isModal == true">
    <div class="white-bg">
      <h4>상세 페이지</h4>
      <p>상세 페이지 내용</p>
    </div>
  </div>
</template>

<script>
import Sales from "./components/Sales.vue";
import Menu from "./components/Menu.vue";
export default {
  name: "App",
  components: {
    Sales,
    Menu,
  },
  data() {
    return {
      isModal: false,
    };
  },
  methods: {
    imgClick() {
      this.isModal = true;
    },
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

.black-bg {
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  padding: 20px;
}

.white-bg {
  width: 100%;
  background: white;
  border-radius: 8px;
  padding: 20px;
}
</style>
