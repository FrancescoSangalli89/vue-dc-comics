<template>
  <div id="app">
    <MyHeader />
    <MyProducts />
    <MyFooter />
  </div>
</template>

<script>

import MyHeader from './components/MyHeader.vue';
import MyProducts from './components/MyProducts.vue';
import MyFooter from './components/MyFooter.vue';

export default {
  name: 'App',
  components: {
    MyHeader,
    MyProducts,
    MyFooter
  }
}
</script>

<style lang="scss">
@import './styles/vars.scss';
@import './styles/general.scss';
@import './styles/typo.scss';
@import './styles/utilities.scss';
</style>
