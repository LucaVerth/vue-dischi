<template>
  <header>
    <div class="header-logo">
      <img src="../assets/img/logo-small.svg" alt="">
    </div>
    <SearchMenu
      @changeGenre="musicGenre"
    />
  </header>
</template>

<script>
import SearchMenu from "./SearchMenu.vue";

export default {
  name: 'Header',
  data(){
    return{
      genreToSend: '',
    }
  },
  components:{
    SearchMenu,
  },
  methods:{
    musicGenre(data){
      this.genreToSend = data;
      //console.log(this.genreToSend);
      this.$emit('musicGenre', this.genreToSend);
    }
  }
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

header{
  @include align();
  justify-content: space-between;
  height: 70px;
  background-color: $primary-color;
  .header-logo {
  width: 60px;
  height: 60px;
  padding: 10px;
  }
  .filter {
    padding: 20px;
  }
}

</style>