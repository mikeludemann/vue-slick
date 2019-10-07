<template lang="html">
  <section id="slick">

  </section>
</template>

<script>
import Vue from "vue";
import $ from "jquery";

import "slick-carousel/slick/slick-theme.css";
import "slick-carousel/slick/slick.css";
import "slick-carousel/slick/slick.min.js";

const SlickSlider = Vue.component('SlickSlider', {
  props: {
    class: {
      type: String
    },
    options: {
      type: Object
    }
  },
  mounted(){
    $(document).ready(function(){
      $(this.class).slick(this.options);
    });
  },
  data() {
    return {

    }
  },
  methods: {

  },
  computed: {

  },
  template: `
    <div :class="class">
      <slot></slot>
    </div>
  `
});

const SliderElement = Vue.component('SliderElement', {
  props: {},
  mounted(){
    
  },
  data() {
    return {

    }
  },
  methods: {

  },
  computed: {

  },
  template: `
    <div>
      <slot></slot>
    </div>
  `
});

export default  {
  name: 'slick',
  components: {
    SlickSlider,
    SliderElement
  }
}
</script>

<style scoped lang="scss">
  .slick {

  }
</style>
