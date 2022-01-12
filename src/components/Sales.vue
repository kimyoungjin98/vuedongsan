<template>
  <div class="black-bg" v-if="isModal == true">
    <div class="white-bg">
      <h4>상세 페이지</h4>
      <p>상세 페이지 내용</p>
      <button class="modal_close" @click="isModal = false">닫기</button>
    </div>
  </div>
  <div v-for="(sale, index) in sales" :key="index">
    <img :src="sale.image" class="room_img" @click="isModal = true" />
    <h4>{{ sale.title }}</h4>
    <p>{{ sale.price }}</p>
    <button @click="increase(index)">허위매물신고</button
    ><span>신고수 : {{ sale.report }}</span>
  </div>
</template>
<script>
import products from "../data/products";

export default {
  name: "Sales",
  data() {
    return {
      isModal: false,
      sales: products,
    };
  },
  methods: {
    increase(index) {
      this.sales[index].report++;
    },
  },
};
</script>
<style>
.room_img {
  margin-top: 40px;
  width: 50%;
  cursor: pointer;
}

.modal_close {
  width: 50px;
  border: none;
  background-color: skyblue;
  color: white;
  margin: 20px;
}
</style>
