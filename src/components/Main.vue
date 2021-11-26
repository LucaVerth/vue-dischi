<template>
  <main>
    MAIN
    <div class="album-container">
      <div>
        <Cards/>
      </div>
    </div>
  </main>
</template>

<script>
import Cards from "./Cards.vue";

export default {
  components:{
    Cards,
  }
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

main{
  height: calc(100vh - 70px);
  background-color: $secondary-color;
}
</style>