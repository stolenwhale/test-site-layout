<template>
  <div class="gallery">
    <div class="gallery__item" v-for="(item, index) in galleryItems" :key="item + index">
      <ImageSlider :images="item.images" />
      <h2 class="gallery__title">
        {{ item.title }}
      </h2>
      <span class="gallery__desc">
        {{ item.desc }}
      </span>
    </div>
  </div>
</template>

<script>
import ImageSlider from "./ImageSlider";
export default {
  name: "GalleryGrid",
  components: {
    ImageSlider
  },
  data() {
    return {
      galleryItems: [
        {
          title: "Тут 4 картинки",
          desc:
            "Роскошь 17-18 веков. Просторные светлые помещения, натуральное дерево и благородная цветовая палитра.",
          images: [
            `https://via.placeholder.com/396x840`,
            `https://via.placeholder.com/396x840`,
            `https://via.placeholder.com/396x840`,
            `https://via.placeholder.com/396x840`
          ]
        },
        {
          title: "Тут 2 картинки",
          desc:
            "Роскошь 17-18 веков. Просторные светлые помещения, натуральное дерево и благородная цветовая палитра.",
          images: [`https://via.placeholder.com/396x840`, `https://via.placeholder.com/396x840`]
        },
        {
          title: "Тут 1 картинка",
          desc:
            "Роскошь 17-18 веков. Просторные светлые помещения, натуральное дерево и благородная цветовая палитра.",
          images: [`https://via.placeholder.com/396x840`]
        },
        {
          title: "Тут 8 картинок",
          desc:
            "Роскошь 17-18 веков. Просторные светлые помещения, натуральное дерево и благородная цветовая палитра.",
          images: [
            `https://via.placeholder.com/396x840`,
            `https://via.placeholder.com/396x840`,
            `https://via.placeholder.com/396x840`,
            `https://via.placeholder.com/396x840`,
            `https://via.placeholder.com/396x840`,
            `https://via.placeholder.com/396x840`,
            `https://via.placeholder.com/396x840`,
            `https://via.placeholder.com/396x840`
          ]
        }
      ]
    };
  }
};
</script>
