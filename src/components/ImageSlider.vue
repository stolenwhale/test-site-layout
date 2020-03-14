<template>
  <div
    class="gallery_image-slider image-slider"
    @mouseover="hover = true"
    @mouseleave="hover = false"
  >
    <transition name="fade">
      <!--            <div class="image_slider__nav">-->
      <div class="image_slider__nav" v-if="images.length > 1 && hover">
        <div
          v-for="buttonIndex in images.length"
          :key="buttonIndex"
          @mouseover="currentImage = buttonIndex"
          :class="{
            'image-slider__button': true,
            'image-slider__button_active': buttonIndex === currentImage
          }"
        ></div>
      </div>
    </transition>
    <div class="image-slider__image-wrapper" v-for="(image, index) in images" :key="index + image">
      <transition name="fade">
        <img class="image-slider__image" :src="image" v-if="index === currentImage - 1" />
      </transition>
    </div>
  </div>
</template>

<script>
export default {
  name: "ImageSlider",
  props: {
    images: Array
  },
  data() {
    return {
      hover: false,
      currentImage: 1
    };
  }
};
</script>
