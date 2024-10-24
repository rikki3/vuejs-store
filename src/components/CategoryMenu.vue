<template>
    <div>
        <h1>Hello world!</h1>
        <span>
            Welcome to the Vue.js portfolio of<br/>
            Rickesh Darsan Singh!
        </span>
    </div>
    <div>
        <swiper
    :modules="modules"
    :slides-per-view="1"
    :space-between="50"
    navigation
    :pagination="{ clickable: true }"
    :scrollbar="{ draggable: true }"
    :loop="true"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
  >
        <swiper-slide>
            <img src="../assets/logo.png"/><br/>
            <h3>
                Slide 1
            </h3>
        </swiper-slide>
        <swiper-slide>
            <img src="../assets/logo.png"/><br/>
            <h3>
                Slide 2
            </h3>
        </swiper-slide>
        <swiper-slide>
            <img src="../assets/logo.png"/><br/>
            <h3>
                Slide 3
            </h3>
        </swiper-slide>
    </swiper>
    </div>
</template>

<script>
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';

  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
      };
    },
  };
</script>

<style></style>