<template>
  <div id="app">
    <div class="wrapper">
      <Slider />
      <hr />
      <Gallery />
      <hr />
      <Discount />
    </div>
  </div>
</template>

<script>
import Slider from "./components/Slider";
import Gallery from "./components/Gallery";
import Discount from "./components/Discount";

export default {
  name: "App",
  components: {
    Slider,
    Gallery,
    Discount
  }
};
</script>
