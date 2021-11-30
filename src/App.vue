<template>
  <div id="app">
    <div class="main-wrapper">
      <div class="container-fluid">
        <Header
        @musicGenre="genreReceived"
        />
        <Main
        :musicGenre="Genre"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";

export default {
  name: 'App',
  data(){
    return{
      Genre: '',
    }
  },
  components: {
    Header,
    Main,
  },
  methods: {
    genreReceived(data){
      this.Genre = data;
    }
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
