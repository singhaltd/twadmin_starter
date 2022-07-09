<template>
  <swiper
    class="swiper"
    :modules="modules"
    direction="horizontal"
    :slides-per-view="7"
    :space-between="23"
    @swiper="setSwiperRef"
    @resize="handleResize"
  >
    <swiper-slide class="slide py-2" v-for="i in 10" :key="i">
      <CardProduct />
    </swiper-slide>
  </swiper>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import SwiperClass, { Navigation } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";

export default defineComponent({
  name: "swiper-example-change-direction",
  title: "Change direction",
  url: import.meta.url,
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    let swiperRef: SwiperClass | null = null;
    const setSwiperRef = (swiper: SwiperClass) => {
      swiperRef = swiper;
    };

    const handleResize = () => {
      swiperRef?.changeDirection(
        window.innerWidth <= 960 ? "vertical" : "horizontal"
      );
    };

    return {
      modules: [Navigation],
      setSwiperRef,
      handleResize,
    };
  },
});
</script>

