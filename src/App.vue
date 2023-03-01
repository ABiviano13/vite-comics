
<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter
  },

  data(){
    return {

    }
  }
}
</script>

<template>

  <div class="container">
    <AppHeader></AppHeader>
  </div>
  <AppMain></AppMain>
  
</template>

<style lang="scss">
@use './style/general.scss';
</style>
