<template>
  <div class="discount">
    <h2 class="discount__title">Акции</h2>
    <div class="discount__grid">
      <FlipCard
        class="discount__card"
        v-for="discountItem in discounts"
        :key="discountItem.date + discountItem.desc"
        :discountItem="discountItem"
      />
    </div>

    <button class="discount__open-discount-btn brown-btn">Смотреть все</button>
  </div>
</template>

<script>
import FlipCard from "./DiscountFlipCard";
export default {
  name: "Discount",
  components: {
    FlipCard
  },
  data() {
    return {
      discounts: [
        {
          date: new Date(2011, 12, 31),
          desc: "При заказе любой двери фурнитура и плинтуса со скидкой 30%",
          conditions: "При заказе любой двери фурнитура и плинтуса со скидкой 30%",
          img: `https://via.placeholder.com/396x400`
        },
        {
          date: new Date(2011, 12, 31),
          desc: "При заказе любой двери фурнитура и плинтуса со скидкой 30%",
          conditions: "При заказе любой двери фурнитура и плинтуса со скидкой 30%",
          img: `https://via.placeholder.com/396x400`
        },
        {
          date: new Date(2011, 12, 31),
          desc: "При заказе любой двери фурнитура и плинтуса со скидкой 30%",
          conditions: "При заказе любой двери фурнитура и плинтуса со скидкой 30%",
          img: `https://via.placeholder.com/396x400`
        },
        {
          date: new Date(2011, 12, 31),
          desc: "При заказе любой двери фурнитура и плинтуса со скидкой 3аказе любой двери фурнитура и плинтуса со скидкой 3аказе любой двери фурнитура и плинтуса со скидкой 3аказе любой двери фурнитура и плинтуса со скидкой 30%",
          conditions: "При заказе любой двери фурнитура и плинтуса со скидкой 30%",
          img: `https://via.placeholder.com/396x400`
        }
      ]
    };
  }
  // computed: {
  // isMobile() {
  //   return (
  //     screen.width <= 768 ||
  //     /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)
  //   );
  // }
  // }
};
</script>
