<template>
  <div class="menu">
    <!-- <a v-for="(menu, index) in nav" :key="index">{{ menu }}{{ index }}</a> -->
    <a v-for="menu in nav" :key="menu">{{ menu }}</a>
  </div>
</template>
<script>
export default {
  name: "Menu",
  data() {
    return {
      nav: ["Home", "Shop", "About"],
    };
  },
};
</script>
<style>
.menu {
  background-color: cornflowerblue;
  padding: 15px;
  border-radius: 15px;
}

.menu a {
  color: white;
  padding: 10px;
}
</style>
