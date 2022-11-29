<template>
  <div>
    <HeaderPage @selectgen="onSelect" />
    <MainPage :selectedfilter="filtered" />
  </div>
</template>

<script>
import HeaderPage from '@/components/HeaderPage.vue';
import MainPage from '@/components/MainPage.vue';

export default {
  components: {
    HeaderPage,
    MainPage,
  },

  data() {
    return {
      filtered: 'all',
    };
  },

  methods: {
    onSelect(value) {
      this.filtered = value;
      console.log(value);
    },
  },

};
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap";
</style>
