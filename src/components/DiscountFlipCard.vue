<template>
  <div class="flip-card">
    <div class="flip-card_container" @mouseover="hover">
      <div class="flip-card_front" ref="front">
        <img class="discount-card__image" :src="discountItem.img" :alt="discountItem.desc" />
        <span class="discount-card__date">до {{ date }}</span>
        <span class="discount-card__desc">{{ discountItem.desc }}</span>
      </div>
      <div class="flip-card_back" ref="back">
        <span class="discount-card__conditions">{{ discountItem.conditions }}</span>
        <span class="discount-card__date">до {{ date }}</span>
        <button class="discount-card_read-more-btn brown-btn">Подробнее</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FlipCard",
  props: {
    discountItem: Object
  },
  computed: {
    date() {
      let date = this.discountItem.date;
      return `${date.getDate()}.${date.getMonth()}.${date.getFullYear()}`;
    }
  },
  methods: {
    hover() {
      let cardHeight = (0 - this.$refs.front.clientHeight + "px").toString();
      this.$refs.back.style.top = cardHeight;
    }
  }
};
</script>
