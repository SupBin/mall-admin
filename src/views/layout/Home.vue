<template>
  <div class="home">
    <left-menu/>
    <div :class="{ 'main-app': true, 'menu-unfold': $store.state.collapsed }">
        <slider-list/>
    </div>

  </div>
</template>

<script>
import LeftMenu from '@/views/layout/components/menu.vue';
import SliderList from '@/views/layout/components/sliderNav.vue';

export default {
  components: {
    LeftMenu,
    SliderList,

  },
  data() {
    return {

    };
  },
  methods: {
    toggleCollapsed() {
      this.collapsed = !this.collapsed;
    },
  },
};
</script>

<style lang = "less">
@import url("~@/assets/css/home.less");
</style>
