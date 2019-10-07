<template>
  <div class="about">
    <SlickSlider 
      class="main-slider"
      options="{
        infinite: true,
        slidesToShow: 3,
        slidesToScroll: 3
      }"
    >
      <SliderElement>
        1-1
      </SliderElement>
      <SliderElement>
        2-1
      </SliderElement>
      <SliderElement>
        3-1
      </SliderElement>
    </SlickSlider>
  </div>
</template>

<script>
import { Component, Vue } from 'vue-property-decorator';
import { SlickSlider, SliderElement } from '@/components/slick.vue'; // @ is an alias to /src

@Component({
  components: {
    SlickSlider,
    SliderElement
  },
})
export default class About extends Vue {}
</script>