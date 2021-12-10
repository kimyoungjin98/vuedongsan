<template>
  <div v-for="(sale, index) in sales" :key="index">
    <img src="../assets/room0.jpg" class="room_img" />
    <h4>{{ sale.products }}</h4>
    <p>{{ sale.price }} 만원</p>
    <button @click="increase(index)">허위매물신고</button
    ><span>신고수 : {{ sale.report }}</span>
  </div>
</template>
<script>
export default {
  name: "Sales",
  props: {
    isModal: Boolean,
  },
  data() {
    return {
      sales: [
        {
          products: "역삼동원룸",
          price: "60",
          report: 0,
          img: "./assets/room0.jpg",
        },
        {
          products: "천호동원룸",
          price: "40",
          report: 0,
          img: "./assets/room1.jpg",
        },
        {
          products: "마포구원룸",
          price: "50",
          report: 0,
          img: "./assets/room2.jpg",
        },
      ],
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
</style>
