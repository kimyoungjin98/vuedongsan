<template>
  <div class="black-bg" v-if="isModal == true">
    <div class="white-bg">
      <h4>상세 페이지</h4>
      <p>상세 페이지 내용</p>
    </div>
  </div>
</template>
<script>
export default {
  name: "Modal",
  props: {
    isModal: Boolean,
  },
};
</script>
<style>
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
