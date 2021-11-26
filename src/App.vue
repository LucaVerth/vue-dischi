<template>
  <div id="app">
    <div class="main-wrapper">
      <div class="container-fluid">
        <Header/>
        <Main/>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";

export default {
  name: 'App',
  components: {
    Header,
    Main,
  }
}
</script>

<style lang="scss">
@import './assets/style/vars.scss';
@import './assets/style/mixins.scss';
@import './assets/style/generals.scss';

.main-wrapper {
  min-height: 100vh;
}

</style>
